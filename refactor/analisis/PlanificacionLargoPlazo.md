# Planificación a Largo Plazo

## Objetivo General
Desarrollar y desplegar una plataforma de gestión de alacena funcional como MVP en ≤30h, priorizando registro/login, gestión y visualización de inventario, y dejando funcionalidades avanzadas (IA, notificaciones, exportación, IoT) para releases posteriores o como mock/documentación.

---

## Estado Actual (2024-07-18)
- [x] 14 historias del MVP completadas
- [ ] 5 historias del MVP pendientes
- [x] Refactor global de agentes IA, autenticación y UI completado
- [x] Logado permanente y autorrelleno de lista implementados
- [x] Traducciones corregidas y desplegadas

## Fases del Proyecto

### Fase 1: Análisis y Diseño (Semana 1) ✅
- [x] Revisión de requisitos y PRD
- [x] Refinamiento de historias de usuario y backlog priorizado (MVP)
- [x] Definición de criterios de aceptación y alcance del MVP

### Fase 2: Configuración de Entorno y Mock API (Semana 1) ✅
- [x] Configuración de repositorio y entorno de desarrollo
- [x] Implementación de JSON Server para mock de la API
- [x] Documentación de endpoints y ejemplos OpenAPI

### Fase 3: Desarrollo MVP Backend (Semana 1-2) ✅
- [x] Implementación de Supabase Auth y tablas principales
- [x] Políticas RLS y seguridad básica
- [x] Endpoints CRUD para productos
- [x] Despliegue inicial en Supabase

### Fase 4: Desarrollo MVP Frontend (Semana 2-3) 🔄
- [x] Desarrollo de la interfaz web en Python
- [x] Integración con Supabase Auth y CRUD de productos
- [x] Visualización de inventario y feedback de usuario
- [ ] Completar integración IA y PWA

### Fase 5: Pruebas y QA (Semana 3) 🔄
- [x] Pruebas unitarias básicas completadas
- [ ] Pruebas de integración en curso
- [ ] Validación final de criterios de aceptación del MVP
- [ ] Corrección de bugs pendientes

### Fase 6: Despliegue y Mantenimiento (Semana 3+) 🔄
- [x] Despliegue en entorno productivo (Supabase)
- [x] Documentación básica
- [ ] Soporte y mejoras continuas
- [ ] Planificación detallada de próximas funcionalidades

---

## Hitos Principales

- [x] **Semana 1:** MVP funcional (registro, login, gestión y visualización de inventario) en entorno de pruebas
- [x] **Semana 2:** MVP desplegado en Supabase, feedback inicial y QA básico
- [ ] **Semana 3:** Documentación, integración IA y cierre de la primera versión

---

## Riesgos y Mitigaciones

- [x] **Desalineación de requisitos:** Revisión y refinamiento continuo del backlog - MITIGADO
- [x] **Problemas de integración:** Uso de Supabase y documentación OpenAPI - RESUELTO
- [ ] **Retrasos en desarrollo IA:** Priorización estricta del MVP y entregas incrementales - EN GESTIÓN

---

## Próximos Pasos Priorizados

1. Completar integración de agentes IA (HU_24, HU_25)
2. Implementar PWA y funcionalidad offline (HU_22)
3. Finalizar selector de estilo (HU_21)
4. Implementar edición y eliminación de categorías (HU_26)
5. Completar pruebas de integración y QA

> [2024-07-18] Hito: Refactor global completado. Siguiente foco en integración IA y PWA.
