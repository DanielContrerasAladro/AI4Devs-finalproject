# Backlog Priorizado (MoSCoW)

> **Nota:** El primer paso es la [tarea de inicialización y Hola Mundo](../../README.md), imprescindible para arrancar el proyecto y sobre la que dependen el resto de historias de usuario.

> **Nota:** El MVP (≤30h) incluye solo las historias imprescindibles para una app funcional y desplegada en Supabase. El resto se implementará en releases posteriores o como mock/documentación.

## Must Have (MVP)
- [] HU_1: Registro de usuario *(MVP)*
- [] HU_2: Inicio de sesión *(MVP)*
- [X] **HU_3: Gestión de productos en la alacena *(MVP, foco inicial de desarrollo)***
- [X] **HU_4: Visualización de inventario *(MVP, foco inicial de desarrollo)***
- [X] HU_5: Añadir y quitar productos del inventario *(MVP)*

## Should Have (Mock/Parcial en MVP, completo en releases posteriores)
- HU_6: Edición de perfil de usuario *(Mock/Parcial en MVP)*
- HU_7: Recomendaciones de IA para menús *(Mock/Parcial en MVP)*
- HU_8: Generación automática de lista de la compra *(Mock/Parcial en MVP)*

## Could Have (Solo diseño/mock en MVP, completo en releases posteriores)
- HU_9: Personalización de notificaciones *(Mock/Parcial en MVP)*
- HU_10: Exportar datos de la alacena *(Mock/Parcial en MVP)*

## Won't Have (por ahora, solo endpoint/documentación en MVP)
- HU_11: Integración con dispositivos IoT *(Solo endpoint/documentación en MVP)*

> **Nota de priorización:** El equipo comenzará el desarrollo del MVP por las historias HU_3 (Gestión de productos) y HU_4 (Visualización de inventario), ya que son el núcleo funcional de la aplicación y habilitan el resto de funcionalidades clave.

### Avances recientes
- [X] Modelo de datos y relaciones implementados en Supabase.
- [X] Políticas RLS aplicadas y probadas.
- [X] Endpoints REST funcionales para productos y listas.
- [X] Integración inicial frontend-backend en Reflex.