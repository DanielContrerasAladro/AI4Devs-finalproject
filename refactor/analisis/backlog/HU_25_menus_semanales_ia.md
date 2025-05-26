# Historia de Usuario: Menús semanales con IA y comidas fuera

Como usuario,
quiero planificar menús semanales con ayuda de IA e indicar los días que como fuera,
para organizar mejor mis comidas y compras.

## Criterios de Aceptación (Gherkin)

```gherkin
Feature: Menús semanales con IA y comidas fuera
  Scenario: Planificación de menú semanal
    Given que accedo a la sección de menús
    When planifico la semana
    Then puedo marcar los días que como fuera y recibir sugerencias de menús de IA para el resto
```

## Notas técnicas
- Integración con IA y gestión visual de calendario.

## Desglose Técnico y Estimación de Tareas

- Frontend (FE): M
- Backend (BE): M
- QA: S

| Rol  | Responsable | Observaciones |
|------|-------------|--------------|
| FE   | FE_MenusIA   |              |
| BE   | BE_MenusIA   |              |
| QA   | QA_MenusIA   |              |
| PO   | PO_MenusIA   | Validación de criterios de aceptación |
| BA   | BA_MenusIA   | Validación de requisitos y coherencia |

## QA/PO: Criterios de aceptación y pruebas

- QA: Preparar casos de prueba para cada criterio de aceptación.
- PO: Validar que la funcionalidad cumple los criterios definidos.
- QA: Documentar resultados de pruebas y feedback.
