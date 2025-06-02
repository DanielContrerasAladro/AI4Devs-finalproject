# Planificación a Largo Plazo

## Objetivo General
Desarrollar y desplegar una plataforma de gestión de alacena funcional como MVP en ≤30h, priorizando registro/login, gestión y visualización de inventario, y dejando funcionalidades avanzadas (IA, notificaciones, exportación, IoT) para releases posteriores o como mock/documentación.

---

## Fases del Proyecto

### Fase 1: Análisis y Diseño (Semana 1)
- Revisión de requisitos y PRD.
- Refinamiento de historias de usuario y backlog priorizado (MVP).
- Definición de criterios de aceptación y alcance del MVP.

### Fase 2: Configuración de Entorno y Mock API (Semana 1)
- Configuración de repositorio y entorno de desarrollo.
- Implementación de JSON Server para mock de la API (solo si es necesario para frontend).
- Documentación de endpoints y ejemplos OpenAPI.

### Fase 3: Desarrollo MVP Backend (Semana 1-2)
- Implementación de Supabase Auth y tablas principales (usuarios, productos).
- Políticas RLS y seguridad básica.
- Endpoints CRUD para productos.
- Despliegue inicial en Supabase.

### Fase 4: Desarrollo MVP Frontend (Semana 2-3)
- Desarrollo de la interfaz web en Python (PyScript/Anvil).
- Integración con Supabase Auth y CRUD de productos.
- Visualización de inventario y feedback de usuario.

### Fase 5: Pruebas y QA (Semana 3)
- Pruebas unitarias y de integración mínimas.
- Validación de criterios de aceptación del MVP.
- Corrección de bugs y mejoras.

### Fase 6: Despliegue y Mantenimiento (Semana 3+)
- Despliegue en entorno productivo (Supabase Hosting).
- Documentación y soporte básico.
- Planificación de mejoras y nuevas funcionalidades (Should/Could/Won't Have).

---

## Hitos Principales

- **Semana 1:** MVP funcional (registro, login, gestión y visualización de inventario) en entorno de pruebas.
- **Semana 2:** MVP desplegado en Supabase, feedback inicial y QA básico.
- **Semana 3:** Documentación, mock de funcionalidades avanzadas y cierre de la primera versión.

---

## Riesgos y Mitigaciones

- **Desalineación de requisitos:** Revisión y refinamiento continuo del backlog.
- **Problemas de integración:** Uso de Supabase y documentación OpenAPI.
- **Retrasos en desarrollo:** Priorización estricta del MVP y entregas incrementales.

- Implementar gestión avanzada de categorías (edición y eliminación) [HU_26] en releases posteriores al MVP.
