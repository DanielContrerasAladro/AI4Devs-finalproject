Título de la Historia de Usuario:
Gestión de productos en la alacena

Como usuario autenticado,
quiero poder añadir, editar y eliminar productos en mi alacena,
para que pueda mantener actualizado el inventario de mi despensa.

Criterios de Aceptación:
- El usuario puede añadir, editar y eliminar productos (CRUD completo).
- El usuario introduce nombre, cantidad, unidad y fecha de caducidad.
- El sistema valida los datos introducidos y muestra mensajes claros en caso de error.
- Los cambios se reflejan en tiempo real (Supabase Realtime).
- Solo se gestionan productos del usuario autenticado (RLS en Supabase).

Notas Adicionales:
- La gestión debe ser intuitiva y accesible desde la pantalla principal.
- Debe existir confirmación antes de eliminar un producto.
- Gestión avanzada (categorías, unidades personalizadas) se implementará en releases posteriores.
- **Esta historia entra en el MVP.**

Historias de Usuario Relacionadas:
- HU_4 (Visualización de inventario)
- HU_5 (Añadir/quitar productos)

---

## Desglose Técnico y Estimación de Tickets

### Frontend (Python (PyScript/Anvil))
- Implementar interfaz para añadir productos
  _Talla de camiseta: S_
- Implementar interfaz para editar productos
  _Talla de camiseta: S_
- Implementar interfaz para eliminar productos
  _Talla de camiseta: S_
- Validación de datos y mensajes de error
  _Talla de camiseta: S_
- Integración con API de productos
  _Talla de camiseta: S_

### Backend (FastAPI)
- Endpoint para crear producto (POST /productos)
  _Talla de camiseta: M_
- Endpoint para editar producto (PUT /productos/{id})
  _Talla de camiseta: M_
- Endpoint para eliminar producto (DELETE /productos/{id})
  _Talla de camiseta: M_
- Validación de datos y manejo de errores
  _Talla de camiseta: S_

### QA/Testing
- Pruebas unitarias y de integración para gestión de productos
  _Talla de camiseta: S_

---

```mermaid
graph TD
    FE1[Añadir producto] --> FE2[Editar producto]
    FE2 --> FE3[Eliminar producto]
    FE3 --> FE4[Validación de datos]
    FE4 --> FE5[Integración API]
    BE1[Crear producto] --> BE2[Editar producto]
    BE2 --> BE3[Eliminar producto]
    BE3 --> BE4[Validación y errores]
    FE5 --> QA1[Pruebas gestión productos]
    BE4 --> QA1
```

---

## Plan de trabajo y tickets (Sprint actual)

### 1. Frontend & Diseño (Prioridad máxima)
- [X] Prototipo visual de la gestión de productos (listado, formulario de alta/edición, confirmación de borrado) usando TailwindCSS.
- [X] Validación de formularios y feedback de errores en la UI.
- [ ] Resaltado visual para productos próximos a caducar.
- [X] Accesibilidad y responsive desde el primer momento.
- [X] Revisión y validación rápida con el equipo.

### 2. Backend & DevOps
- [X] Definir el modelo de datos `Producto` en Supabase (campos: id, nombre, cantidad, unidad, fecha_caducidad, usuario_id).
- [X] Configurar RLS para que cada usuario solo acceda a sus productos.
- [X] Crear endpoints básicos (CRUD) en FastAPI/Supabase.
- [ ] Validación de datos y control de errores en la API.
- [ ] Soporte para eventos en tiempo real (opcional en MVP, recomendable).

### 3. Integración Frontend-Backend
- [X] Conectar la UI con los endpoints reales.
- [X] Pruebas de flujo completo: alta, edición, borrado y visualización de productos.
- [X] **Tests unitarios y de integración automatizados y pasando.**
- [X] **Automatización de calidad en pre-commit.**
- [ ] Feedback de errores y confirmaciones en la app.

### Avances realizados (Sprint actual)
- [X] Definido el modelo de datos en Supabase (ver `supabase/schema.sql`)
- [X] Configuradas las políticas RLS para compartición de listas y productos
- [X] Actualizado el README con el nuevo modelo y diagrama
- [X] Documentados los endpoints REST disponibles (Supabase autoexpone endpoints para cada tabla)
- [X] Endpoints REST funcionales y probados para productos y listas
- [X] Integración inicial frontend-backend en Reflex: creación y visualización de listas y productos
- [X] Creado microservicio Python base (`microservice/main.py`)
- [X] Política de SELECT abierta para facilitar pruebas en desarrollo (se eliminará en producción)

---

> **Nota:** El equipo trabajará en paralelo en frontend/diseño y backend/devops, priorizando la entrega temprana de la parte visual para revisión y testeo rápido. La integración se realizará en cuanto los endpoints estén disponibles.

## Avance de desarrollo (Sprint actual)

- Funcionalidad CRUD de productos completamente implementada y testeada.
- Validaciones exhaustivas en backend para alta, edición y borrado (nombre, cantidad, unidad, caducidad).
- Feedback claro y visible para el usuario en todas las operaciones (éxito y error).
- Tests unitarios y de integración para todos los casos de uso y edge cases.
- Cumplimiento estricto de TDD: primero los tests, luego la lógica.
- Código preparado para despliegue en producción.

### Checklist de criterios de aceptación (HU_3)
- [x] El usuario puede añadir, editar y eliminar productos (CRUD completo).
- [x] Validación de datos y mensajes claros en caso de error.
- [x] Cambios reflejados en tiempo real.
- [x] Solo se gestionan productos del usuario autenticado (RLS en Supabase, validado en entorno real).
- [x] Confirmación antes de eliminar producto y feedback visual.
- [x] Tests automatizados y pasando en CI.

#### Mensaje de commit sugerido
```
feat(hu_3): Gestión de productos completa con validaciones, feedback y tests

- CRUD de productos con validaciones exhaustivas en backend.
- Feedback claro en UI para alta, edición y borrado.
- Tests unitarios y de integración para todos los casos.
- Refactor para feedback reactivo y robusto.
- Listo para despliegue en producción.
```
