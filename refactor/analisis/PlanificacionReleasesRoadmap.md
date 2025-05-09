# Planificación de Releases y Roadmap

## Release 1: MVP - Gestión Básica de Alacena (Semana 1-5)
- HU_1: Registro de usuario
- HU_2: Inicio de sesión
- HU_3: Gestión de productos en la alacena
- HU_4: Visualización de inventario
- HU_5: Añadir y quitar productos del inventario

## Release 2: Personalización y Planificación Inteligente (Semana 6-8)
- HU_6: Edición de perfil de usuario
- HU_7: Recomendaciones de IA para menús
- HU_8: Generación automática de lista de la compra

## Release 3: Funcionalidades Avanzadas (Semana 9-10)
- HU_9: Personalización de notificaciones
- HU_10: Exportar datos de la alacena

## Release 4: Integración y Automatización (Post-MVP)
- HU_11: Integración con dispositivos IoT

---

## Roadmap Visual

```mermaid
gantt
    dateFormat  YYYY-MM-DD
    title       Roadmap Alacena

    section MVP
    Registro e inicio de sesión         :done,    r1, 2024-07-01, 10d
    Gestión de productos e inventario   :done,    r2, 2024-07-11, 15d

    section Personalización y IA
    Edición de perfil                   :active,  r3, 2024-07-26, 5d
    Recomendaciones IA y lista compra   :         r4, 2024-07-31, 10d

    section Avanzado
    Notificaciones y exportación        :         r5, 2024-08-10, 7d

    section Futuro
    Integración IoT                     :         r6, 2024-08-17, 14d
