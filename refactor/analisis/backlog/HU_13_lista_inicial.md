# Historia de Usuario: Lista de la compra obligatoria e inicial

Como usuario nuevo,
quiero que al registrarme se cree automáticamente una lista de la compra inicial y obligatoria,
para poder empezar a usar la app sin configuraciones manuales.

## Criterios de Aceptación (Gherkin)

```gherkin
Feature: Lista de la compra inicial
  Scenario: Registro de usuario
    Given que me registro por primera vez
    Then la app crea automáticamente una lista de la compra asociada a mi cuenta
    And no puedo eliminar esta lista (es obligatoria)
```

## Notas técnicas
- La lista debe crearse en el backend al registrar usuario.
- No debe poder eliminarse, pero sí editarse y añadir productos.

## Desglose Técnico y Estimación de Tareas

- Frontend (FE): S
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
