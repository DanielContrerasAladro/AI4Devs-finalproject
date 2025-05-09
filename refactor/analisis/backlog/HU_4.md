Título de la Historia de Usuario:
Visualización de inventario

Como usuario autenticado,
quiero visualizar el inventario de mi alacena,
para que pueda conocer en todo momento los productos disponibles y su estado.

Criterios de Aceptación:
- El usuario puede ver una lista de todos los productos de su alacena.
- Se muestran detalles como nombre, cantidad y fecha de caducidad.
- Los productos próximos a caducar se resaltan visualmente.
- El usuario puede buscar y filtrar productos por nombre o categoría.

Notas Adicionales:
- La visualización debe ser clara y ordenada.
- Debe existir opción de ordenar por fecha de caducidad o cantidad.

Historias de Usuario Relacionadas:
- HU_3 (Gestión de productos en la alacena)
- HU_5 (Añadir/quitar productos)

---

## Desglose Técnico y Estimación de Tickets

### Frontend (Python (PyScript/Anvil))
- Implementar vista de inventario con listado de productos
  _Talla de camiseta: S_
- Implementar resaltado visual para productos próximos a caducar
  _Talla de camiseta: S_
- Implementar búsqueda y filtrado de productos
  _Talla de camiseta: S_
- Implementar ordenación por fecha de caducidad o cantidad
  _Talla de camiseta: S_

### Backend (FastAPI)
- Endpoint para obtener listado de productos (GET /productos)
  _Talla de camiseta: M_
- Lógica para filtrar, buscar y ordenar productos
  _Talla de camiseta: S_

### QA/Testing
- Pruebas unitarias y de integración para visualización de inventario
  _Talla de camiseta: S_

---

```mermaid
graph TD
    FE1[Vista inventario] --> FE2[Resaltado caducidad]
    FE2 --> FE3[Búsqueda y filtrado]
    FE3 --> FE4[Ordenación]
    FE4 --> BE1[Listado productos API]
    BE1 --> BE2[Lógica filtrado/orden]
    FE4 --> QA1[Pruebas visualización]
    BE2 --> QA1
