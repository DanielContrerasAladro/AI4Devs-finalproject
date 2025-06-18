# Apartados y funcionalidades pendientes de desarrollo

Este documento recoge las tareas pendientes por cada área de la aplicación.

---

## Páginas principales

### 1. Autenticación
- [x] Login (src/app/auth/login_view.py) - COMPLETADO
- [x] Estado de login y persistencia (src/app/auth/login_state.py) - COMPLETADO
- [x] Logado permanente (auto-login) - IMPLEMENTADO
- [ ] Recuperación de contraseña - PENDIENTE
- [ ] Registro de usuario (si aplica) - PENDIENTE

### 2. Inventario
- [x] Visualización de inventario (src/app/pages/inventory.py) - COMPLETADO
- [x] Resaltado de productos próximos a caducar - IMPLEMENTADO
- [x] Ordenación y filtrado básico - COMPLETADO
- [ ] Ordenación y filtrado avanzado - PENDIENTE
- [x] Feedback visual de errores y confirmaciones - IMPLEMENTADO

### 3. Productos
- [x] CRUD de productos (src/app/products/) - COMPLETADO
- [x] Edición rápida (+/-) - IMPLEMENTADO
- [x] Gestión de iconos y categorías - COMPLETADO
- [x] Eliminación con confirmación - IMPLEMENTADO
- [x] Validaciones básicas - COMPLETADO
- [ ] Validaciones avanzadas - PENDIENTE

### 4. Listas de la compra
- [x] Visualización y gestión de listas (src/app/lists/) - COMPLETADO
- [x] Autorrelleno de lista según inventario - IMPLEMENTADO
- [ ] Compartición de listas - PENDIENTE
- [ ] Edición y eliminación de categorías - PENDIENTE

### 5. Menús
- [ ] Planificación semanal (src/app/pages/menus.py) - EN DESARROLLO
- [ ] Integración con IA para sugerencias - PENDIENTE
- [ ] Marcar días fuera - PENDIENTE

### 6. Recetas
- [ ] Sugerencias de recetas IA (src/app/pages/recipes.py) - PENDIENTE
- [ ] Añadir ingredientes a la lista de la compra - PENDIENTE

### 7. Internacionalización
- [x] Selector de idioma (src/app/i18n/) - COMPLETADO
- [ ] Selector de tema - PENDIENTE
- [x] Corrección bug i18n en producción - COMPLETADO

### 8. PWA
- [ ] Instalación y funcionalidad offline - PENDIENTE
- [ ] Manifest y service worker - PENDIENTE

### 9. Componentes y UI
- [ ] Unificación de estilos (src/app/components/) - EN DESARROLLO
- [ ] Accesibilidad y responsive - PENDIENTE

---

## Agentes y Orquestador IA

### 1. Orquestador IA
- [ ] Integración completa con backend y frontend (src/app/api/orchestrator/orchestrator.py) - PENDIENTE
- [ ] Gestión de contexto y flujo de mensajes - PENDIENTE

### 2. Agente IA Nutricional
- [ ] Generación de menús y recetas (src/app/api/agents/nutritional.py) - PENDIENTE
- [ ] Personalización según usuario - PENDIENTE

### 3. Agente IA de Hábitos
- [ ] Análisis de hábitos y feedback (src/app/api/agents/habits.py) - PENDIENTE

### 4. Agente IA Inventario/Alertas
- [x] Gestión de inventario y alertas (src/app/api/agents/inventory.py) - COMPLETADO
- [x] Notificaciones de caducidad - IMPLEMENTADO

### 5. LLM Loader / MCP
- [ ] Integración y pruebas de LLM loader (src/app/api/agents/llm_loader.py) - PENDIENTE

---

## Utilidades y otros
- [x] Helpers y utilidades comunes (src/app/utils/) - COMPLETADO
- [x] Tests unitarios básicos - COMPLETADO
- [ ] Tests de integración pendientes - EN DESARROLLO
- [ ] QA y validación de criterios de aceptación - EN DESARROLLO

---

> [2024-07-18] Actualización: Completadas funcionalidades base y autenticación. Próximo foco en integración IA y PWA.
