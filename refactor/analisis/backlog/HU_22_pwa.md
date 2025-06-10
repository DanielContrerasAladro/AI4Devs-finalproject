# Historia de Usuario: Instalación PWA

Como usuario,
quiero poder instalar la aplicación como PWA en mi dispositivo,
para acceder rápidamente y usarla como una app nativa.

## Criterios de Aceptación (Gherkin)

```gherkin
Feature: Instalación PWA
  Scenario: Instalación en dispositivo
    Given que accedo a la app desde un navegador compatible
    When selecciono la opción de instalar
    Then la app se instala correctamente y es accesible desde el menú de apps
```

## Notas técnicas
- Manifest y service worker configurados correctamente.
- Test en diferentes dispositivos.

## Desglose Técnico y Estimación de Tareas

- Frontend (FE): S
- Backend (BE): S
- QA: S

| Rol  | Responsable | Observaciones |
|------|-------------|--------------|
| FE   | FE_PWA   |              |
| BE   | BE_PWA   |              |
| QA   | QA_PWA   |              |
| PO   | PO_PWA   | Validación de criterios de aceptación |
| BA   | BA_PWA   | Validación de requisitos y coherencia |

## QA/PO: Criterios de aceptación y pruebas

- QA: Preparar casos de prueba para cada criterio de aceptación.
- PO: Validar que la funcionalidad cumple los criterios definidos.
- QA: Documentar resultados de pruebas y feedback.

---

> Prioridad alta en el roadmap tras reunión de planificación 2024-07-17. Esta HU se abordará tras las funcionalidades de IA, reservando además un 20% del tiempo de sprint para revisión de bugs y corrección de funcionalidad actual.
