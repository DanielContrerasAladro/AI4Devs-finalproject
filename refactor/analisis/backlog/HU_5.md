Título de la Historia de Usuario:
Añadir y quitar productos del inventario

Como usuario autenticado,
quiero poder añadir o quitar unidades de productos en mi alacena,
para que el inventario refleje siempre la cantidad real disponible.

Criterios de Aceptación:
- El usuario puede incrementar o disminuir la cantidad de un producto existente.
- El sistema no permite cantidades negativas.
- El usuario recibe confirmación tras cada operación.
- El registro de movimientos es mock/simplificado en el MVP (historial avanzado en releases posteriores).

Notas Adicionales:
- Debe ser posible realizar estas acciones desde la vista de inventario.
- El historial de movimientos completo se implementará en releases posteriores.
- **Esta historia entra en el MVP.**

Historias de Usuario Relacionadas:
- HU_3 (Gestión de productos en la alacena)
- HU_4 (Visualización de inventario)

---

## Desglose Técnico y Estimación de Tickets

### Frontend (Python (PyScript/Anvil))
- [X] Implementar botones para añadir y quitar unidades en la vista de inventario
  _Talla de camiseta: S_
- [X] Validación para evitar cantidades negativas
  _Talla de camiseta: S_
- [X] Mostrar confirmación tras cada operación
  _Talla de camiseta: S_
- [X] Visualización del historial de movimientos (mock MVP)
  _Talla de camiseta: S_

### Backend (FastAPI)
- [X] Endpoint para registrar movimiento de producto (POST /movimientos)
  _Talla de camiseta: M_
- [X] Lógica para actualizar cantidad y validar límites
  _Talla de camiseta: S_
- [X] Endpoint para obtener historial de movimientos (GET /movimientos) (mock MVP)
  _Talla de camiseta: S_

### QA/Testing
- [X] Pruebas unitarias y de integración para movimientos de inventario
  _Talla de camiseta: S_
- [X] Automatización de tests y calidad en pre-commit
  _Talla de camiseta: S_
- [X] Validación de edge cases: no permitir cantidades negativas, feedback de errores
  _Talla de camiseta: S_

---

**Avances implementados:**
- La funcionalidad de añadir y quitar productos está completamente operativa desde la vista de inventario.
- El sistema valida que no se puedan introducir cantidades negativas y muestra confirmaciones y errores claros.
- El historial de movimientos está disponible como mock en el MVP.
- Los tests unitarios y de integración cubren los flujos principales y edge cases, y están automatizados en el flujo de calidad.

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
