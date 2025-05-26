# Historia de Usuario: Alertas y visualización avanzada de caducidades

Como usuario,
quiero recibir alertas y ver claramente los productos próximos a caducar,
para evitar desperdicio y gestionar mejor mi inventario.

## Criterios de Aceptación (Gherkin)

```gherkin
Feature: Alertas de caducidad
  Scenario: Visualización de productos próximos a caducar
    Given que visualizo mi inventario
    Then los productos próximos a caducar se resaltan visualmente

  Scenario: Recepción de alertas
    Given que tengo productos próximos a caducar
    Then recibo una notificación o alerta en la app
```

## Notas técnicas
- Resaltado visual y notificaciones push/email.

## Desglose Técnico y Estimación de Tareas

- Frontend (FE): S
- Backend (BE): S
- QA: S

| Rol  | Responsable | Observaciones |
|------|-------------|--------------|
| FE   | FE_Productos   |              |
| BE   | BE_Productos   |              |
| QA   | QA_Productos   |              |
| PO   | PO_Productos   | Validación de criterios de aceptación |
| BA   | BA_Productos   | Validación de requisitos y coherencia |

## QA/PO: Criterios de aceptación y pruebas

- QA: Preparar casos de prueba para cada criterio de aceptación.
- PO: Validar que la funcionalidad cumple los criterios definidos.
- QA: Documentar resultados de pruebas y feedback.
