# Backlog Priorizado (MoSCoW)

> **Nota:** El MVP (≤30h) incluye solo las historias imprescindibles para una app funcional y desplegada en Supabase. El resto se implementará en releases posteriores o como mock/documentación.

## Must Have (MVP) - Estado actual
- [x] HU_1: Registro de usuario *(MVP)*
- [x] HU_2: Inicio de sesión *(MVP)*
- [x] HU_3: Gestión de productos en la alacena *(MVP)*
- [x] HU_4: Visualización de inventario *(MVP)*
- [x] HU_5: Añadir y quitar productos del inventario *(MVP)*
- [x] HU_13: Lista de la compra obligatoria e inicial *(MVP)*
- [x] HU_14: Listas personalizables y compartibles *(MVP)*
- [x] HU_15: Iconos y categorías en productos *(MVP)*
- [x] HU_16: Alertas y visualización avanzada de caducidades *(MVP)*
- [x] HU_17: Mover productos entre listas *(MVP)*
- [x] HU_18: Edición rápida de productos (+ y -) *(MVP)*
- [x] HU_19: Botón de eliminar producto visible *(MVP)*
- [x] HU_20: Logado permanente *(MVP)*
- [x] HU_23: Autorrelleno automático de la lista de la compra *(MVP)*
- [ ] HU_12: Ajuste y coherencia del layout base *(MVP)* - En progreso
- [ ] HU_21: Selector de idioma y estilo personalizable *(MVP)* - Traducciones completadas
- [ ] HU_22: Instalación PWA *(MVP)*
- [ ] HU_24: Recetas IA y autorrelleno de lista de la compra *(MVP)*
- [ ] HU_25: Menús semanales con IA y comidas fuera *(MVP)*

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

### Estado actual del proyecto (2024-07-18)
- [x] 14 historias completadas del MVP
- [ ] 5 historias pendientes del MVP
- [x] Refactor global de agentes IA, autenticación y UI completado
- [x] Logado permanente y autorrelleno de lista implementados
- [x] Traducciones corregidas y desplegadas

### Próximos pasos priorizados
1. HU_24: Recetas IA y autorrelleno de lista de la compra
2. HU_25: Menús semanales con IA
3. HU_22: Instalación PWA
4. HU_21: Completar selector de estilo
5. HU_26: Edición y eliminación de categorías

> [2024-07-18] Se mantiene un 20% del tiempo de sprint para revisión de bugs y corrección de funcionalidad actual.

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
