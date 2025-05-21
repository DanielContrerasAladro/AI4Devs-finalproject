Título de la Historia de Usuario:
Visualización de inventario

Como usuario autenticado,
quiero visualizar el inventario de mi alacena,
para que pueda conocer en todo momento los productos disponibles y su estado.

Criterios de Aceptación:
- El usuario puede ver una lista clara y ordenada de todos los productos de su alacena.
- Se muestran detalles como nombre, cantidad, unidad y fecha de caducidad.
- Los productos próximos a caducar se resaltan visualmente.
- El usuario puede buscar y filtrar productos por nombre o categoría.
- La visualización es responsive y accesible.

Notas Adicionales:
- La visualización avanzada (gráficas, agrupaciones) se implementará en releases posteriores.
- **Esta historia entra en el MVP.**

Historias de Usuario Relacionadas:
- HU_3 (Gestión de productos en la alacena)
- HU_5 (Añadir/quitar productos)

---

## Plan de trabajo y tickets (Sprint actual)

### 1. Frontend & Diseño (Prioridad máxima)
- [X] Prototipo visual de la vista de inventario (listado de productos, detalles, resaltado de caducidad) usando TailwindCSS.
- [X] Implementar búsqueda y filtrado en la lista.
- [ ] Ordenación por fecha de caducidad o cantidad.
- [X] Accesibilidad y responsive.
- [X] Revisión y validación rápida con el equipo.

### 2. Backend & DevOps
- [ ] Endpoint para obtener listado de productos (`GET /productos`) con soporte de filtros y orden.
- [ ] Lógica para filtrar, buscar y ordenar productos en la API.
- [ ] Pruebas unitarias e integración de la consulta de inventario.

### 3. Integración Frontend-Backend
- [ ] Conectar la vista de inventario con el endpoint real.
- [X] Pruebas de visualización, búsqueda y filtrado.
- [ ] Feedback visual para productos próximos a caducar.

---

> **Nota:** El foco inicial es entregar una vista de inventario usable y visualmente atractiva, integrando la lógica de backend en cuanto esté disponible.

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
