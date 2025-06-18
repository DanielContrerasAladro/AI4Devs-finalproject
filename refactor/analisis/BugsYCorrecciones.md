# Registro de Bugs y Correcciones

Este documento sirve para registrar y hacer seguimiento de bugs, incidencias y correcciones necesarias, organizadas por página y por agente.

---

## Páginas principales

### 1. Autenticación
- **Bugs detectados:**
  - [x] La página inicial debe ser /lists en lugar de / al hacer login - CORREGIDO
- **Correcciones propuestas:**
  - [x] Redirigir a /lists cuando el login sea correcto - IMPLEMENTADO

### 2. Inventario
- **Bugs detectados:**
  - [x] El módulo para poder añadir un elemento, en lugar de estar en la raíz, debe estar en /lists - CORREGIDO
- **Correcciones propuestas:**
  - [x] Mover el módulo de página - IMPLEMENTADO

### 3. Productos
- **Bugs detectados:**
  - [x] Añadir un nuevo elemento no está cargando las listas en el seleccionable - CORREGIDO
  - [x] No funciona la selección de ícono para la categoría - CORREGIDO
  - [x] Hay que tener cuidado para que las modales se muestren siempre con un z-index superior - CORREGIDO
  - [x] Debe de poder ser fácil añadir o eliminar la cantidad con botones '+' y '-' - IMPLEMENTADO
- **Correcciones propuestas:**
  - [x] Todas las correcciones implementadas y validadas

### 4. Listas de la compra
- **Bugs detectados:**
  - [x] La lista de la compra debe existir siempre y ser la primera seleccionada - CORREGIDO
  - [x] Quitar las coletillas IA de cualquier botón de la aplicación - CORREGIDO
- **Correcciones propuestas:**
  - [x] Todas las correcciones implementadas y validadas

### 5. Menús
- **Bugs detectados:**
  - [x] Error en MenuState ('get_user_id') - CORREGIDO
  - [ ] El botón 'Generar menú semanal' no funciona correctamente
- **Correcciones propuestas:**
  - [ ] Implementar integración con agente IA para menús semanales

### 6. Recetas
- **Bugs detectados:**
  - [ ] La pantalla debería mostrar un listado de las recetas guardadas
  - [ ] Error en 'RecipesState' ('get_user_id')
  - [ ] El botón 'Añadir ingredientes faltantes' no funciona correctamente
- **Correcciones propuestas:**
  - [ ] Implementar integración con agente IA para recetas

### 7. Internacionalización
- **Bugs detectados:**
  - [x] Términos incorrectamente traducidos - CORREGIDO
- **Correcciones propuestas:**
  - [x] Revisión y corrección de traducciones - IMPLEMENTADO
  - [ ] Pendiente implementar selector de estilo

### 8. PWA
- **Bugs detectados:**
  - [x] Login no persistente - CORREGIDO
  - [ ] La aplicación debe ser instalable como PWA
- **Correcciones propuestas:**
  - [x] Implementación de logado permanente y refresh de token - COMPLETADO
  - [ ] Implementar manifest y service worker para PWA

### 9. Componentes y UI
- **Bugs detectados:**
  - [ ] La pantalla del orquestador no mantiene el layout consistente
- **Correcciones propuestas:**
  - [ ] Unificar estilos y layout en todas las pantallas

---

## Agentes y Orquestador IA

### 1. Orquestador IA
- **Bugs detectados:**
  - [ ] Error de autenticación al usar el chat IA
- **Correcciones propuestas:**
  - [ ] Integrar autenticación con el orquestador IA

### 2. Agente IA Nutricional
- **Bugs detectados:**
  - [ ] Error de autenticación al generar menús
- **Correcciones propuestas:**
  - [ ] Integrar autenticación con el agente nutricional

### 3. Agente IA de Hábitos
- **Bugs detectados:**
  - [ ] Error de autenticación al generar informes
- **Correcciones propuestas:**
  - [ ] Integrar autenticación con el agente de hábitos

### 4. Agente IA Inventario/Alertas
- **Bugs detectados:**
  - [x] Autorrelleno de lista de la compra no funcionaba - CORREGIDO
- **Correcciones propuestas:**
  - [x] Implementación de autorrelleno automático - COMPLETADO

### 5. LLM Loader / MCP
- **Bugs detectados:**
  - [ ] Integración pendiente con los agentes
- **Correcciones propuestas:**
  - [ ] Implementar integración con todos los agentes

---

> [2024-07-18] Actualización: Completadas correcciones críticas de autenticación, UI y funcionalidad base. Próximo foco en integración IA y PWA.
