# Backlog Priorizado (MoSCoW)

> **Nota:** El MVP (≤30h) incluye solo las historias imprescindibles para una app funcional y desplegada en Supabase. El resto se implementará en releases posteriores o como mock/documentación.

## Must Have (MVP)
- HU_1: Registro de usuario *(MVP)*
- HU_2: Inicio de sesión *(MVP)*
- HU_3: Gestión de productos en la alacena *(MVP)*
- HU_4: Visualización de inventario *(MVP)*
- HU_5: Añadir y quitar productos del inventario *(MVP)*

## Should Have (Mock/Parcial en MVP, completo en releases posteriores)
- HU_6: Edición de perfil de usuario *(Mock/Parcial en MVP)*
- HU_7: Recomendaciones de IA para menús *(Mock/Parcial en MVP)*
- HU_8: Generación automática de lista de la compra *(Mock/Parcial en MVP)*
- HU_26: Edición y eliminación de categorías *(Release próximo)*

## Could Have (Solo diseño/mock en MVP, completo en releases posteriores)
- HU_9: Personalización de notificaciones *(Mock/Parcial en MVP)*
- HU_10: Exportar datos de la alacena *(Mock/Parcial en MVP)*

## Won't Have (por ahora, solo endpoint/documentación en MVP)
- HU_11: Integración con dispositivos IoT *(Solo endpoint/documentación en MVP)*

- **HU: Edición y eliminación de categorías**
  - Como usuario quiero poder editar y eliminar categorías para mantener mi lista de categorías organizada y actualizada.
  - **Criterios de aceptación:**
    - El usuario puede editar el nombre y el icono de una categoría existente.
    - El usuario puede eliminar una categoría, con advertencia si tiene productos asociados.
    - No se permite eliminar la categoría "Sin categoría".
    - Los productos afectados se actualizan automáticamente.
    - Feedback visual de éxito o error.
  - **Tareas técnicas:**
    - Crear panel/listado de categorías con opciones de editar y eliminar.
    - Implementar eventos y lógica para editar/eliminar categorías en backend y frontend.
    - Gestionar actualización reactiva de productos afectados.
    - Añadir tests para edición y eliminación de categorías.
