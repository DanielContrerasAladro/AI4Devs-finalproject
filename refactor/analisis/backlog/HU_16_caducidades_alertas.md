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

| Rol  | Responsable | Estado |
|------|-------------|---------|
| FE   | FE_Productos   | Completado |
| BE   | BE_Productos   | Completado |
| QA   | QA_Productos   | Completado |
| PO   | PO_Productos   | Validado |
| BA   | BA_Productos   | Validado |

## QA/PO: Criterios de aceptación y pruebas

- [x] QA: Casos de prueba para cada criterio de aceptación completados.
- [x] PO: Funcionalidad validada y cumple los criterios definidos.
- [x] QA: Resultados de pruebas y feedback documentados.

---

## [2024-07-18] Cierre de historia

La HU_16 ha sido completada, validada y desplegada en producción. El resaltado visual de productos próximos a caducar está funcionando correctamente y ha sido validado por QA y PO. La funcionalidad está disponible para los usuarios finales.
