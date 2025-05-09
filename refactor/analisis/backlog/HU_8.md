Título de la Historia de Usuario:
Generación automática de lista de la compra

Como usuario autenticado,
quiero que la aplicación genere automáticamente una lista de la compra basada en mis menús y productos faltantes,
para que pueda realizar mis compras de manera eficiente y sin olvidar ingredientes necesarios.

Criterios de Aceptación:
- El sistema identifica productos faltantes en función de los menús planificados y el inventario actual.
- El usuario puede revisar, modificar y aprobar la lista antes de guardarla o exportarla.
- La lista puede ser exportada o compartida fácilmente.
- El sistema sugiere cantidades recomendadas según el consumo habitual.

Notas Adicionales:
- La generación debe ser accesible desde la sección de menús o inventario.
- Debe existir opción de añadir productos manualmente a la lista.

Historias de Usuario Relacionadas:
- HU_7 (Recomendaciones de IA para menús)
- HU_3 (Gestión de productos en la alacena)

---

## Desglose Técnico y Estimación de Tickets

### Frontend (Python (PyScript/Anvil))
- Implementar interfaz para mostrar y editar la lista de la compra
  _Talla de camiseta: M_
- Permitir añadir productos manualmente a la lista
  _Talla de camiseta: S_
- Opción para exportar o compartir la lista
  _Talla de camiseta: S_
- Integración con API de generación de lista
  _Talla de camiseta: S_

### Backend (FastAPI)
- Endpoint para generar lista de la compra (GET /lista-compra/generar)
  _Talla de camiseta: L_
- Lógica para identificar productos faltantes y sugerir cantidades
  _Talla de camiseta: M_
- Endpoint para exportar lista (GET /lista-compra/exportar)
  _Talla de camiseta: S_

### QA/Testing
- Pruebas unitarias y de integración para generación y exportación de lista
  _Talla de camiseta: M_

---

```mermaid
graph TD
    FE1[Mostrar/editar lista] --> FE2[Añadir productos manualmente]
    FE2 --> FE3[Exportar/compartir lista]
    FE3 --> FE4[Integración API lista]
    BE1[Generar lista compra] --> BE2[Lógica productos faltantes]
    BE2 --> BE3[Exportar lista]
    FE4 --> QA1[Pruebas lista compra]
    BE3 --> QA1
