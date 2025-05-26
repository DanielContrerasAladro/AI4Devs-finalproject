# Historia de Usuario: Mover productos entre listas

Como usuario,
quiero poder mover productos entre diferentes listas de la compra,
para organizar mis compras según mis necesidades.

## Criterios de Aceptación (Gherkin)

```gherkin
Feature: Mover productos entre listas
  Scenario: Mover producto
    Given que tengo varias listas
    When selecciono un producto
    And elijo la opción de mover
    Then puedo seleccionar la lista destino y el producto se traslada correctamente
```

## Notas técnicas
- Soporte drag & drop o menú contextual.

## Desglose Técnico y Estimación de Tareas

- Frontend (FE): M
- Backend (BE): S
- QA: S

| Rol  | Responsable | Observaciones |
|------|-------------|--------------|
| FE   | FE_Listas   |              |
| BE   | BE_Listas   |              |
| QA   | QA_Listas   |              |
| PO   | PO_Listas   | Validación de criterios de aceptación |
| BA   | BA_Listas   | Validación de requisitos y coherencia |

## QA/PO: Criterios de aceptación y pruebas

- QA: Preparar casos de prueba para cada criterio de aceptación.
- PO: Validar que la funcionalidad cumple los criterios definidos.
- QA: Documentar resultados de pruebas y feedback.
