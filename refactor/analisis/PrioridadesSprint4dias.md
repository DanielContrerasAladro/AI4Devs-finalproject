# Priorización Sprint 4 días: MVP, Bugs y Pendientes

Este documento recoge la priorización de tareas y bugs para el sprint de 4 días antes de la salida a producción. Se ha realizado un match entre los apartados pendientes, los bugs detectados y lo considerado como MVP, aplicando la metodología MoSCoW y buenas prácticas de desarrollo.

---

## Leyenda MoSCoW
- **[MUST]**: Imprescindible para el MVP y la salida a producción.
- **[SHOULD]**: Muy recomendable, mejora la experiencia o la calidad, pero no bloquea el MVP.
- **[COULD]**: Deseable, pero puede posponerse si no hay tiempo.
- **[WON'T]**: No se abordará en este sprint.

## Leyenda Tallas
- **XS**: <1h
- **S**: 1-2h
- **M**: 2-4h
- **L**: 4-8h
- **XL**: >8h

---

## Prioridades por área

### 1. Autenticación
- [MUST] Redirigir a /lists tras login correcto (bug) — **S** — _Responsable: Frontend_
- [MUST] Logado permanente (auto-login, token refresh) — **M** — _Responsable: Frontend_
- [WON'T] Recuperación de contraseña — **S** — _Responsable: Backend_

### 2. Inventario y Productos
- [MUST] Mover el módulo de añadir elemento a /lists (bug) — **S** — _Responsable: Frontend_
- [MUST] CRUD de productos funcional y validado — **M** — _Responsable: Backend_
- [MUST] Selección de lista al añadir producto (bug) — **S** — _Responsable: Frontend_
- [MUST] Selección de icono para categoría, y alta de categoría (bug) — **S** — _Frontend_
- [MUST] CRUD de productos, alimentos, funcional y validado — **M** — _Backend_
- [MUST] Edición rápida (+/-) en listado de productos, alimento (bug) — **S** — _Frontend_
- [COULD] Resaltado de productos próximos a caducar — **S** — _Responsable: Frontend_
- [WON'T] Ordenación y filtrado avanzado — **M** — _Responsable: Frontend_

### 3. Listas de la compra
- [MUST] La lista de la compra debe existir siempre y ser la primera seleccionada (bug) — **S** — _Backend_
- [MUST] Autorrelleno de lista según inventario (MVP) — **M** — _AI Engineer_
- [MUST] Quitar coletillas IA de botones — **XS** — _Responsable: Frontend_
- [COULD] Compartición de listas — **M** — _Responsable: Backend_
- [WON'T] Edición y eliminación de categorías — **M** — _Responsable: Backend_

### 4. Menús y Recetas
- [MUST] Corregir error en MenuState ('get_user_id') (bug) — **S** — _Responsable: Backend_
- [MUST] El botón 'Generar menú semanal' debe funcionar y actualizar el menú (bug/MVP) — **M** — _Responsable: AI Engineer_
- [MUST] El botón 'Sugerir receta' debe funcionar y mostrar receta (bug/MVP) — **M** — _Responsable: AI Engineer_
- [MUST] El botón 'Añadir ingredientes faltantes' debe funcionar (bug/MVP) — **S** — _Responsable: Backend_
- [COULD] Mostrar listado de recetas guardadas y permitir edición — **M** — _Responsable: Backend_
- [WON'T] Marcar días fuera en planificación semanal — **S** — _Responsable: Frontend_

### 5. Internacionalización
- [MUST] Corregir traducción de términos (bug) — **S** — _Responsable: Frontend_

### 6. PWA y Accesibilidad
- [MUST] Login persistente y refresco de token (bug/MVP) — **M** — _Responsable: Frontend_
- [MUST] Manifest y service worker revisados — **S** — _Responsable: DevOps_
- [COULD] La app debe ser instalable como PWA (bug/MVP) — **S** — _Responsable: DevOps_
- [COULD] Accesibilidad y responsive — **S** — _Responsable: Diseñador_

### 7. Componentes y UI
- [MUST] Unificación de estilos y coherencia visual (bug orquestador más ancho) — **S** — _Responsable: Diseñador_

### 8. Agentes y Orquestador IA
- [SHOULD] Los agentes IA deben responder correctamente en /lists (nutricional, hábitos, inventario/alertas) (bug) — **M** — _Responsable: AI Engineer_
- [SHOULD] El orquestador debe funcionar y responder en /orquestador (bug) — **M** — _Responsable: AI Engineer_
- [SHOULD] LLM Loader/MCP debe ser llamado y probado — **S** — _Responsable: AI Engineer_

### 9. QA y Tests
- [SHOULD] Tests unitarios y de integración para los flujos críticos — **M** — _Responsable: QA_
- [COULD] QA y validación de criterios de aceptación — **S** — _Responsable: QA_

---

## Listado de tareas técnicas por prioridad

### Tareas MUST
- [DONE] Redirigir a /lists tras login correcto (bug) — **S** — _Frontend_
- [DONE] Logado permanente (auto-login, token refresh) — **M** — _Frontend_
- [DONE] Mover el módulo de añadir elemento a /lists (bug) — **S** — _Frontend_
- [DONE] Selección de lista al añadir producto (bug) — **S** — _Frontend_
- [DONE] Login persistente y refresco de token (bug/MVP) — **M** — _Frontend_
- [DONE] Selección de icono para categoría, y alta de categoría (bug) — **S** — _Frontend_
- [DONE] CRUD de productos, alimentos, funcional y validado — **M** — _Backend_
- [DONE] Edición rápida (+/-) en listado de productos, alimento (bug) — **S** — _Frontend_
- [DONE] Corregir error en MenuState ('get_user_id') (bug) — **S** — _Backend_
- [DONE] La lista de la compra debe existir siempre y ser la primera seleccionada (bug) — **S** — _Backend_
- [DONE] Autorrelleno de lista según inventario (MVP) — **M** — _AI Engineer_
- [DONE] Limpieza de trazas en el código - **XS** - _Backend_ & _Frontend_
- [DONE] Quitar coletillas IA de botones — **XS** — _Frontend_
- [DONE] Corregir traducción de términos (bug) — **S** — _Frontend_
- [DONE] Resaltado de productos próximos a caducar — **S** — _Frontend_

### Tareas SHOULD
- Ordenación y filtrado avanzado en inventario — **M** — _Responsable: Frontend + Backend_
- Mostrar listado de recetas guardadas y permitir edición — **M** — _Backend_
- Unificación de estilos y coherencia visual (bug orquestador más ancho) — **S** — _Diseñador_
- Accesibilidad y responsive — **S** — _Diseñador_
- Compartir listas con otros usuarios — **M** — _Backend_
- El botón 'Sugerir receta' debe funcionar y mostrar receta (bug/MVP) — **M** — _AI Engineer_
- El botón 'Añadir ingredientes faltantes' debe funcionar (bug/MVP) — **S** — _Backend_
- El botón 'Generar menú semanal' debe funcionar y actualizar el menú (bug/MVP) — **M** — _AI Engineer_
- El orquestador debe funcionar y responder en /orquestador (bug) — **M** — _AI Engineer_
- Los agentes IA deben responder correctamente en /lists (nutricional, hábitos, inventario/alertas) (bug) — **M** — _AI Engineer_

### Tareas COULD
- Manifest y service worker revisados — **S** — _DevOps_
- La app debe ser instalable como PWA (bug/MVP) — **S** — _DevOps_
- LLM Loader/MCP debe ser llamado y probado — **S** — _AI Engineer_
- Tests unitarios y de integración para los flujos críticos — **M** — _QA_
- QA y validación de criterios de aceptación — **S** — _QA_

---

## Resumen de tareas que podrían quedar fuera (WON'T)
- Mejoras visuales no esenciales — **S** — _Responsable: Diseñador + Frontend_
- Personalización avanzada de notificaciones — **M** — _Responsable: Backend + Frontend_
- Funcionalidades avanzadas de IA no críticas para el MVP — **L** — _Responsable: AI Engineer + Backend_
- Exportación de datos — **M** — _Responsable: Backend + Frontend_
- Integración IoT — **L** — _Responsable: Backend + DevOps_

---

> Esta priorización debe ser revisada y validada por el equipo antes de comenzar el sprint. Marca cada tarea según se aborde o se decida posponer.
