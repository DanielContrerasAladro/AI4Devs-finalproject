# Historia de Usuario: Edición y eliminación de categorías

Como usuario,
quiero poder editar y eliminar categorías para mantener mi lista de categorías organizada y actualizada.

## Criterios de Aceptación (Gherkin)

```gherkin
Feature: Gestión de categorías
  Scenario: Editar categoría
    Given que visualizo la lista de categorías
    When selecciono una categoría existente
    Then puedo modificar su nombre y su icono
    And los productos asociados se actualizan automáticamente

  Scenario: Eliminar categoría
    Given que visualizo la lista de categorías
    When selecciono la opción de eliminar en una categoría
    Then recibo una advertencia si tiene productos asociados
    And si confirmo, la categoría se elimina y los productos pasan a "Sin categoría"
    And no se permite eliminar la categoría "Sin categoría"
    And recibo feedback visual de éxito o error
```

## Notas técnicas
- Panel/listado de categorías con opciones de editar y eliminar.
- Edición de nombre e icono de categoría.
- Eliminación de categoría con advertencia si tiene productos asociados.
- No permitir eliminar la categoría "Sin categoría".
- Actualización reactiva de productos afectados.
- Feedback visual de éxito o error.
- Tests para edición y eliminación de categorías.

## Desglose Técnico y Estimación de Tareas

- Frontend (FE): M
- Backend (BE): M
- QA: S

| Rol  | Responsable | Observaciones |
|------|-------------|--------------|
| FE   | FE_Categorías   |              |
| BE   | BE_Categorías   |              |
| QA   | QA_Categorías   |              |
| PO   | PO_Categorías   | Validación de criterios de aceptación |
| BA   | BA_Categorías   | Validación de requisitos y coherencia |

## QA/PO: Criterios de aceptación y pruebas

- QA: Preparar casos de prueba para cada criterio de aceptación.
- PO: Validar que la funcionalidad cumple los criterios definidos.
- QA: Documentar resultados de pruebas y feedback.
