Título de la Historia de Usuario:
Registro de usuario

Como usuario nuevo,
quiero registrarme en la aplicación,
para que pueda gestionar mi alacena de forma personalizada.

Criterios de Aceptación:
- El usuario puede introducir nombre, email y contraseña.
- El sistema valida que el email no esté registrado (unicidad).
- El usuario recibe feedback inmediato de éxito o error.
- El registro está integrado con Supabase Auth.
- El usuario puede iniciar sesión tras registrarse.

Notas Adicionales:
- El registro social (Google) es opcional y se implementará en releases posteriores.
- El registro debe ser sencillo y accesible desde la pantalla principal.
- **Esta historia entra en el MVP.**

Historias de Usuario Relacionadas:
- HU_2 (Inicio de sesión)

---

## Desglose Técnico y Estimación de Tickets

### Frontend (Python (PyScript/Anvil))
- **Implementar formulario de registro de usuario**
  _Talla de camiseta: S_
- **Validación de campos y mensajes de error**
  _Talla de camiseta: S_
- **Integración con API de registro**
  _Talla de camiseta: S_

### Backend (FastAPI)
- **Endpoint de registro de usuario (POST /usuarios)**
  _Talla de camiseta: M_
- **Validación de unicidad de email y lógica de negocio**
  _Talla de camiseta: S_
- **Envío de respuesta y manejo de errores**
  _Talla de camiseta: S_

### QA/Testing
- **Pruebas unitarias y de integración para el registro**
  _Talla de camiseta: S_

---

```mermaid
graph TD
    FE1[Formulario de registro] --> FE2[Validación de campos]
    FE2 --> FE3[Integración API]
    BE1[Endpoint registro usuario] --> BE2[Validación email]
    BE2 --> BE3[Manejo de errores]
    FE3 --> QA1[Pruebas de registro]
    BE3 --> QA1
```

[Volver a la tarea de inicialización y Hola Mundo](../../README.md)
