# Backlog Priorizado (MoSCoW)

> **Nota:** El primer paso es la [tarea de inicialización y Hola Mundo](../../README.md), imprescindible para arrancar el proyecto y sobre la que dependen el resto de historias de usuario.

> **Nota:** El MVP (≤30h) incluye solo las historias imprescindibles para una app funcional y desplegada en Supabase. El resto se implementará en releases posteriores o como mock/documentación.

## Must Have (MVP)
- HU_1: Registro de usuario *(MVP)*
- HU_2: Inicio de sesión *(MVP)*
- HU_3: Gestión de productos en la alacena *(MVP)*
- HU_4: Visualización de inventario *(MVP)*
- HU_5: Añadir y quitar productos del inventario *(MVP)*
- HU_12: Ajuste y coherencia del layout base *(MVP)*
- HU_13: Lista de la compra obligatoria e inicial *(MVP)*@
- HU_14: Listas personalizables y compartibles *(MVP)*
- HU_15: Iconos y categorías en productos *(MVP)*
- HU_16: Alertas y visualización avanzada de caducidades *(MVP)*
- HU_17: Mover productos entre listas *(MVP)*
- HU_18: Edición rápida de productos (+ y -) *(MVP)*
- HU_19: Botón de eliminar producto visible *(MVP)*
- HU_20: Logado permanente *(MVP)*
- HU_21: Selector de idioma y estilo personalizable *(MVP)*
- HU_22: Instalación PWA *(MVP)*
- HU_23: Autorrelleno automático de la lista de la compra *(MVP)*
- HU_24: Recetas IA y autorrelleno de lista de la compra *(MVP)*
- HU_25: Menús semanales con IA y comidas fuera *(MVP)*

## Should Have (Mock/Parcial en MVP, completo en releases posteriores)
- HU_6: Edición de perfil de usuario *(Mock/Parcial en MVP)*
- HU_7: Recomendaciones de IA para menús *(Mock/Parcial en MVP)*
- HU_8: Generación automática de lista de la compra *(Mock/Parcial en MVP)*

## Could Have (Solo diseño/mock en MVP, completo en releases posteriores)
- HU_9: Personalización de notificaciones *(Mock/Parcial en MVP)*
- HU_10: Exportar datos de la alacena *(Mock/Parcial en MVP)*

## Won't Have (por ahora, solo endpoint/documentación en MVP)
- HU_11: Integración con dispositivos IoT *(Solo endpoint/documentación en MVP)*

## Next Release
- HU_26: Edición y eliminación de categorías *(Release próximo)*

> Ver detalle en [HU_26_editar_eliminar_categorias.md](HU_26_editar_eliminar_categorias.md)

> **Nota de priorización:** El equipo comenzará el desarrollo del MVP por las historias HU_3 (Gestión de productos) y HU_4 (Visualización de inventario), ya que son el núcleo funcional de la aplicación y habilitan el resto de funcionalidades clave.

### Avances recientes
- [X] Modelo de datos y relaciones implementados en Supabase.
- [X] Políticas RLS aplicadas y probadas.
- [X] Endpoints REST funcionales para productos y listas.
- [X] Integración inicial frontend-backend en Reflex.
- [X] **Tests unitarios y de integración automatizados y pasando en CI.**
- [X] **Automatización de calidad: pre-commit con tests, linting y formateo.**
- [X] **Solucionados problemas de imports, mocks y warnings en la batería de tests.**

| Estado      | Historia/Ticket                                      |
|-------------|------------------------------------------------------|
| Por hacer   | HU_12, HU_20, HU_21, HU_22, HU_23, HU_24, HU_25 |
| En progreso |  |
| Hecho       | HU_1, HU_2, HU_3, HU_4, HU_5, HU_13, HU_14, HU_15, HU_16, HU_17, HU_18, HU_19                               |

gantt
    dateFormat  YYYY-MM-DD
    title       Roadmap Alacena

    section MVP
    Registro e inicio de sesión         :done,    r1, 2024-07-01, 3d
    Gestión de productos e inventario   :active,  r2, 2024-07-04, 7d
    Visualización de inventario         :active,  r3, 2024-07-11, 4d
    Ajustes y funcionalidades clave     :         r4, 2024-07-15, 14d

    section Personalización y IA
    Edición de perfil                   :         r5, 2024-07-29, 5d
    Recomendaciones IA y lista compra   :         r6, 2024-08-03, 10d

    section Avanzado
    Notificaciones y exportación        :         r7, 2024-08-13, 7d

    section Futuro
    Integración IoT                     :         r8, 2024-08-20, 14d

> [2024-07-16] Hito: Migración a modelo simplificado de alimentos con lista_id directo, eliminación de la tabla alimentos_listas, refactor de backend y frontend, y validación de la funcionalidad. HU_3 y HU_4 completadas y listas para producción.

> [2024-07-17] Hito: Finalización del bloque @lists. Internacionalización, robustez y corrección de errores en la gestión de listas y alimentos. Listo para commit y despliegue en producción.
