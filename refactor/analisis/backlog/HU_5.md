Título de la Historia de Usuario:
Añadir y quitar productos del inventario

Como usuario autenticado,
quiero poder añadir o quitar unidades de productos en mi alacena,
para que el inventario refleje siempre la cantidad real disponible.

Criterios de Aceptación:
- El usuario puede incrementar o disminuir la cantidad de un producto existente.
- El sistema no permite cantidades negativas.
- Cada movimiento queda registrado con fecha y tipo de operación (entrada/salida).
- El usuario recibe confirmación tras cada operación.

Notas Adicionales:
- Debe ser posible realizar estas acciones desde la vista de inventario.
- El historial de movimientos debe estar disponible para consulta.

Historias de Usuario Relacionadas:
- HU_3 (Gestión de productos en la alacena)
- HU_4 (Visualización de inventario)

---

## Desglose Técnico y Estimación de Tickets

### Frontend (Python (PyScript/Anvil))
- Implementar botones para añadir y quitar unidades en la vista de inventario
  _Talla de camiseta: S_
- Validación para evitar cantidades negativas
  _Talla de camiseta: S_
- Mostrar confirmación tras cada operación
  _Talla de camiseta: S_
- Visualización del historial de movimientos
  _Talla de camiseta: S_

### Backend (FastAPI)
- Endpoint para registrar movimiento de producto (POST /movimientos)
  _Talla de camiseta: M_
- Lógica para actualizar cantidad y validar límites
  _Talla de camiseta: S_
- Endpoint para obtener historial de movimientos (GET /movimientos)
  _Talla de camiseta: S_

### QA/Testing
- Pruebas unitarias y de integración para movimientos de inventario
  _Talla de camiseta: S_

---

```mermaid
graph TD
    FE1[Botones añadir/quitar] --> FE2[Validación cantidad]
    FE2 --> FE3[Confirmación operación]
    FE3 --> FE4[Visualizar historial]
    FE4 --> BE1[Registrar movimiento API]
    BE1 --> BE2[Actualizar cantidad]
    BE2 --> BE3[Obtener historial]
    FE4 --> QA1[Pruebas movimientos]
    BE3 --> QA1
