# Historia de Usuario: Autorrelleno automático de la lista de la compra

Como usuario,
quiero que la lista de la compra se autorrellene automáticamente según los productos que faltan en mi inventario,
para no olvidar ingredientes necesarios al hacer la compra.

## Criterios de Aceptación (Gherkin)

```gherkin
Feature: Autorrelleno de lista de la compra
  Scenario: Productos faltantes detectados
    Given que reviso mi lista de la compra
    When faltan productos habituales en mi inventario
    Then la app los añade automáticamente a la lista de la compra
```

## Notas técnicas
- Integración con inventario y hábitos de compra.

## Desglose Técnico y Estimación de Tareas

- Frontend (FE): S
- Backend (BE): M
- QA: S

| Rol  | Responsable | Observaciones |
|------|-------------|--------------|
| FE   | FE_Autorrelleno   |              |
| BE   | BE_Autorrelleno   |              |
| QA   | QA_Autorrelleno   |              |
| PO   | PO_Autorrelleno   | Validación de criterios de aceptación |
| BA   | BA_Autorrelleno   | Validación de requisitos y coherencia |

## QA/PO: Criterios de aceptación y pruebas

- QA: Preparar casos de prueba para cada criterio de aceptación.
- PO: Validar que la funcionalidad cumple los criterios definidos.
- QA: Documentar resultados de pruebas y feedback.
