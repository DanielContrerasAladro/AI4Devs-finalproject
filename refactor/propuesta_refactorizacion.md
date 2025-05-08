# Propuesta de Refactorización: Alacena PWA (Full Python + Supabase)

## 1. Objetivo

Reescribir Alacena como una aplicación web progresiva (PWA) moderna, responsive, accesible y escalable, utilizando **Supabase** como backend y hosting, y Python tanto para el backend (microservicios, IA) como para el frontend (usando PyScript, Anvil, o similar). Se aprovecharán las capacidades de Supabase para trabajar con datos estructurados (SQL) y semiestructurados (NoSQL/JSONB), y se integrará un agente de IA siguiendo las mejores prácticas y guías oficiales.

---

## 2. Justificación Tecnológica

### 2.1. Por qué Supabase

- **Base de datos relacional (PostgreSQL) con soporte JSONB:** Permite modelar datos complejos y jerárquicos como en NoSQL, pero con la potencia de SQL para análisis y reporting. [Ver ejemplo oficial](https://supabase.com/blog/sql-or-nosql-both-with-postgresql)
- **Open Source y sin vendor lock-in:** Posibilidad de autoalojar en el futuro.
- **Autenticación robusta:** Soporta OAuth, email, social login, etc.
- **Realtime y Edge Functions:** Suscripciones en tiempo real y lógica backend serverless.
- **Almacenamiento integrado:** Para imágenes, documentos, etc.
- **SDK oficial para Python:** Permite integrar lógica avanzada y agentes IA fácilmente ([supabase-py](https://supabase.com/docs/reference/python/introduction)).
- **Precios predecibles:** Basados en almacenamiento y filas, no en operaciones.
- **Integración sencilla con GitHub Actions:** Despliegue automático y CI/CD.

### 2.2. Por qué Python en el Frontend

- **PyScript** y frameworks como **Anvil** permiten crear aplicaciones web modernas usando solo Python, facilitando la curva de aprendizaje para equipos expertos en Python.
- **Reutilización de lógica y modelos** entre backend y frontend.
- **Integración directa con supabase-py** para operaciones de base de datos, autenticación y almacenamiento desde el navegador.
- **Desarrollo rápido de prototipos** y MVPs.

---

## 3. Arquitectura Propuesta

### 3.1. Stack Tecnológico

- **Frontend:** PyScript, Anvil, o similar (PWA, Python en el navegador)
- **UI/UX:** TailwindCSS (integrable con PyScript), componentes personalizados
- **Backend:** Supabase (PostgreSQL, Auth, Storage, Realtime, Edge Functions)
- **IA:** Microservicio Python (Flask/FastAPI) conectado a Supabase y consumido desde el frontend
- **Testing:** Pytest (backend y frontend)
- **CI/CD:** GitHub Actions (build, test, deploy)
- **Internacionalización:** gettext o soluciones Python equivalentes
- **Accesibilidad:** Cumplimiento WCAG 2.1

### 3.2. Diagrama de Arquitectura

```mermaid
flowchart TD
    subgraph Cliente [PWA (PyScript/Anvil)]
        UI[UI/UX (TailwindCSS + Python)]
        Logic[Lógica de Negocio (Python)]
        SW[Service Worker (Offline)]
        IA[Agente IA (API Python)]
    end

    subgraph Backend [Supabase]
        Auth[Auth (OAuth, Email, Social)]
        DB[PostgreSQL DB + JSONB]
        Storage[Storage]
        Edge[Edge Functions]
        Realtime[Realtime]
    end

    UI --> Logic
    Logic -->|Lectura/Escritura| DB
    Logic -->|Gestión de usuarios| Auth
    Logic -->|Subida/Descarga| Storage
    Logic -->|Realtime| Realtime
    Logic -->|Lógica avanzada| Edge
    Logic -->|Recomendaciones| IA
    SW -->|Sincronización| DB

    Cliente -->|Web| Supabase Hosting
    IA -->|API| Backend
```

---

## 4. Ejemplos de Uso de supabase-py

### 4.1. Instalación y Configuración

```python
# Instalar supabase-py
pip install supabase

# Inicializar cliente
from supabase import create_client, Client

url = "https://<your-project>.supabase.co"
key = "<your-anon-or-service-role-key>"
supabase: Client = create_client(url, key)
```
Fuente: [supabase-py docs](https://supabase.com/docs/reference/python/introduction)

### 4.2. Operaciones CRUD

**Insertar datos:**
```python
data = {"name": "Manzana", "cantidad": 5, "caducidad": "2024-07-01"}
res = supabase.table("alimentos").insert(data).execute()
print(res.data)
```

**Leer datos:**
```python
res = supabase.table("alimentos").select("*").eq("name", "Manzana").execute()
print(res.data)
```

**Actualizar datos:**
```python
res = supabase.table("alimentos").update({"cantidad": 10}).eq("name", "Manzana").execute()
print(res.data)
```

**Eliminar datos:**
```python
res = supabase.table("alimentos").delete().eq("name", "Manzana").execute()
print(res.data)
```

### 4.3. Autenticación

```python
# Registro de usuario
res = supabase.auth.sign_up(email="usuario@ejemplo.com", password="contraseña123")
print(res)

# Login de usuario
res = supabase.auth.sign_in(email="usuario@ejemplo.com", password="contraseña123")
print(res)
```

### 4.4. Uso de JSONB y consultas híbridas SQL/NoSQL

Supabase permite almacenar y consultar datos complejos en campos JSONB, combinando lo mejor de SQL y NoSQL.
Ejemplo: almacenar un inventario como JSONB y consultar con SQL avanzado.

```python
# Insertar un registro con un campo JSONB
data = {
    "usuario_id": "xyz",
    "fecha": "2024-07-01",
    "inventario": [
        {"nombre": "Manzana", "cantidad": 5},
        {"nombre": "Leche", "cantidad": 2}
    ]
}
supabase.table("inventarios").insert(data).execute()

# Consultar y descomponer el JSONB en SQL
# (Ejemplo de consulta SQL desde Supabase SQL Editor)
"""
with data as (
  select
    usuario_id,
    fecha,
    jsonb_array_elements(inventario) ->> 'nombre' as nombre,
    (jsonb_array_elements(inventario) -> 'cantidad')::integer as cantidad
  from inventarios
  where usuario_id = 'xyz'
)
select nombre, sum(cantidad) from data group by nombre;
"""
```
Fuente: [SQL or NoSQL? Why not use both (with PostgreSQL)?](https://supabase.com/blog/sql-or-nosql-both-with-postgresql)

---

## 5. Integración de IA y Prompts

Supabase permite integrar IA y prompts directamente en la base de datos o mediante Edge Functions y microservicios Python.
Guía oficial: [Getting Started with AI Prompts](https://supabase.com/docs/guides/getting-started/ai-prompts)

**Ejemplo de integración básica:**
- Guardar prompts y resultados en una tabla de Supabase.
- Llamar a un microservicio Python (Flask/FastAPI) que procese el prompt y devuelva la respuesta.
- Registrar la interacción en la base de datos para análisis posterior.

```python
# Guardar un prompt en la base de datos
prompt = {
    "usuario_id": "xyz",
    "pregunta": "¿Qué menú saludable puedo preparar con manzanas y leche?",
    "respuesta": None,
    "fecha": "2024-07-01"
}
supabase.table("prompts_ia").insert(prompt).execute()
```

**Lógica del microservicio Python:**
```python
from flask import Flask, request, jsonify
from supabase import create_client

app = Flask(__name__)
supabase = create_client(url, key)

@app.route('/ia', methods=['POST'])
def ia():
    data = request.json
    prompt = data['prompt']
    # Aquí se llama a la IA (OpenAI, Gemini, etc.)
    respuesta = generar_respuesta(prompt)
    # Guardar la respuesta en Supabase
    supabase.table("prompts_ia").update({"respuesta": respuesta}).eq("id", data["id"]).execute()
    return jsonify({"respuesta": respuesta})
```
Fuente: [Harnessing the Power of Supabase in Python with supabase-py](https://medium.com/@rohitverma_69543/harnessing-the-power-of-supabase-in-python-with-supabase-py-03f36a97c482)

---

## 6. Estructura de Carpetas Propuesta

```
Alacena/
│
├── frontend/               # PyScript, Anvil, o similar (PWA en Python)
│   ├── static/
│   ├── templates/
│   └── main.py
│
├── ia-service/             # Microservicio Python para IA (Flask/FastAPI + supabase-py)
│   └── app.py
│
├── supabase/               # Configuración y migraciones de Supabase
├── tests/                  # Pytest para backend y frontend
├── .github/workflows/      # CI/CD con GitHub Actions
├── README.md
└── requirements.txt
```

---

## 7. Consideraciones Clave

- **Frontend Python:** Facilita la curva de aprendizaje y la colaboración para equipos expertos en Python.
- **Supabase como backend:** Permite aprovechar lo mejor de SQL y NoSQL, con integración nativa para IA y prompts.
- **Desarrollo ágil:** Prototipado rápido, despliegue sencillo y escalabilidad.
- **IA modular:** El agente IA en Python es desacoplado y evolutivo.
- **Automatización:** CI/CD desde el inicio, con tests automáticos.
- **Seguridad:** Uso de Auth y Row Level Security (RLS) en Supabase.
- **Open Source:** Sin vendor lock-in, posibilidad de autoalojar en el futuro.

---

## 8. Recursos y Referencias

- [supabase-py: documentación oficial](https://supabase.com/docs/reference/python/introduction)
- [Harnessing the Power of Supabase in Python with supabase-py (Medium)](https://medium.com/@rohitverma_69543/harnessing-the-power-of-supabase-in-python-with-supabase-py-03f36a97c482)
- [SQL or NoSQL? Why not use both (with PostgreSQL)?](https://supabase.com/blog/sql-or-nosql-both-with-postgresql)
- [Supabase: Getting Started with AI Prompts](https://supabase.com/docs/guides/getting-started/ai-prompts)

---

**Esta propuesta garantiza una transición ordenada, moderna y escalable, alineada con los objetivos de negocio y técnicos del proyecto Alacena, aprovechando las ventajas de Supabase y su integración con Python.**

> [Log propuesta](log_proceso_propuesta.md)
> [Proceso propuesta](proceso_discusion_propuesta.md)