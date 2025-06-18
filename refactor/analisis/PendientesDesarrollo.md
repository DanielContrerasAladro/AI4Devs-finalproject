# Apartados y funcionalidades pendientes de desarrollo

Este documento recoge, por cada página y agente de la aplicación, los apartados y funcionalidades que faltan por desarrollar o completar según las HU y el estado actual del código.

---

## Páginas principales

### 1. Autenticación
- [ ] Login (src/app/auth/login_view.py)
- [ ] Estado de login y persistencia (src/app/auth/login_state.py)
- [ ] Logado permanente (auto-login)
- [ ] Recuperación de contraseña
- [ ] Registro de usuario (si aplica)

### 2. Inventario
- [ ] Visualización de inventario (src/app/pages/inventory.py)
- [ ] Resaltado de productos próximos a caducar
- [ ] Ordenación y filtrado avanzado
- [ ] Feedback visual de errores y confirmaciones

### 3. Productos
- [ ] CRUD de productos (src/app/products/)
- [ ] Edición rápida (+/-)
- [ ] Gestión de iconos y categorías
- [ ] Eliminación con confirmación
- [ ] Validaciones avanzadas

### 4. Listas de la compra
- [ ] Visualización y gestión de listas (src/app/lists/)
- [ ] Autorrelleno de lista según inventario
- [ ] Compartición de listas
- [ ] Edición y eliminación de categorías

### 5. Menús
- [ ] Planificación semanal (src/app/pages/menus.py)
- [ ] Integración con IA para sugerencias
- [ ] Marcar días fuera

### 6. Recetas
- [ ] Sugerencias de recetas IA (src/app/pages/recipes.py)
- [ ] Añadir ingredientes a la lista de la compra

### 7. Internacionalización
- [ ] Selector de idioma y tema (src/app/i18n/)
- [ ] Corrección bug i18n en producción

### 8. PWA
- [ ] Instalación y funcionalidad offline
- [ ] Manifest y service worker

### 9. Componentes y UI
- [ ] Unificación de estilos (src/app/components/)
- [ ] Accesibilidad y responsive

---

## Agentes y Orquestador IA

### 1. Orquestador IA
- [ ] Integración completa con backend y frontend (src/app/api/orchestrator/orchestrator.py)
- [ ] Gestión de contexto y flujo de mensajes

### 2. Agente IA Nutricional
- [ ] Generación de menús y recetas (src/app/api/agents/nutritional.py)
- [ ] Personalización según usuario

### 3. Agente IA de Hábitos
- [ ] Análisis de hábitos y feedback (src/app/api/agents/habits.py)

### 4. Agente IA Inventario/Alertas
- [ ] Gestión de inventario y alertas (src/app/api/agents/inventory.py)
- [ ] Notificaciones de caducidad

### 5. LLM Loader / MCP
- [ ] Integración y pruebas de LLM loader (src/app/api/agents/llm_loader.py)

---

## Utilidades y otros
- [ ] Helpers y utilidades comunes (src/app/utils/)
- [ ] Tests unitarios y de integración pendientes
- [ ] QA y validación de criterios de aceptación

---

> Actualiza este documento conforme se detecten nuevas tareas o se completen apartados.
