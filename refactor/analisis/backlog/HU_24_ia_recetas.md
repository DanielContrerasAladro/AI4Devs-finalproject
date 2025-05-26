# Historia de Usuario: Recetas IA y autorrelleno de lista de la compra

Como usuario,
quiero que la app sugiera recetas saludables usando IA y rellene la lista de la compra con los ingredientes necesarios,
para planificar mis comidas de forma inteligente y saludable.

## Criterios de Aceptación (Gherkin)

```gherkin
Feature: Recetas IA y lista de la compra
  Scenario: Sugerencia de recetas y autorrelleno
    Given que accedo a la sección de recetas
    When selecciono una receta sugerida por IA
    Then los ingredientes que faltan se añaden automáticamente a la lista de la compra
```

## Notas técnicas
- Integración con motor de IA y lista de la compra.

## Desglose Técnico y Estimación de Tareas

- Frontend (FE): S
- Backend (BE): M
- QA: S

| Rol  | Responsable | Observaciones |
|------|-------------|--------------|
| FE   | FE_IARecetas   |              |
| BE   | BE_IARecetas   |              |
| QA   | QA_IARecetas   |              |
| PO   | PO_IARecetas   | Validación de criterios de aceptación |
| BA   | BA_IARecetas   | Validación de requisitos y coherencia |

## QA/PO: Criterios de aceptación y pruebas

- QA: Preparar casos de prueba para cada criterio de aceptación.
- PO: Validar que la funcionalidad cumple los criterios definidos.
- QA: Documentar resultados de pruebas y feedback.
