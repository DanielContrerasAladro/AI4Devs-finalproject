Título de la Historia de Usuario:
Personalización de notificaciones

Como usuario autenticado,
quiero personalizar las notificaciones que recibo de la aplicación,
para que solo me lleguen avisos relevantes según mis preferencias.

Criterios de Aceptación:
- El usuario puede activar o desactivar notificaciones para diferentes eventos (productos por caducar, recomendaciones, lista de la compra, etc.).
- El usuario puede elegir la frecuencia y el canal de las notificaciones (email, push, etc.).
- El sistema respeta las preferencias configuradas por el usuario.

Notas Adicionales:
- La personalización debe ser accesible desde la configuración del perfil.
- Debe existir opción de restablecer las preferencias a valores por defecto.

Historias de Usuario Relacionadas:
- HU_4 (Visualización de inventario)
- HU_7 (Recomendaciones de IA para menús)

---

## Desglose Técnico y Estimación de Tickets

### Frontend (Python (PyScript/Anvil))
- Implementar interfaz de configuración de notificaciones
  _Talla de camiseta: S_
- Permitir selección de eventos, frecuencia y canal
  _Talla de camiseta: S_
- Opción para restablecer preferencias
  _Talla de camiseta: S_
- Integración con API de notificaciones
  _Talla de camiseta: S_

### Backend (FastAPI)
- Endpoint para guardar preferencias de notificación (POST /notificaciones/preferencias)
  _Talla de camiseta: M_
- Lógica para gestionar eventos, frecuencia y canales
  _Talla de camiseta: M_
- Endpoint para restablecer preferencias
  _Talla de camiseta: S_

### QA/Testing
- Pruebas unitarias y de integración para personalización de notificaciones
  _Talla de camiseta: S_

---

```mermaid
graph TD
    FE1[Configurar notificaciones] --> FE2[Seleccionar eventos/frecuencia/canal]
    FE2 --> FE3[Restablecer preferencias]
    FE3 --> FE4[Integración API notificaciones]
    BE1[Guardar preferencias] --> BE2[Gestión eventos/canales]
    BE2 --> BE3[Restablecer preferencias]
    FE4 --> QA1[Pruebas notificaciones]
    BE3 --> QA1
