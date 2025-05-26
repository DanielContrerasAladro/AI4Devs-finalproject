# Historia de Usuario: Edición rápida de productos (+ y -)

Como usuario,
quiero poder modificar la cantidad de productos con botones + y - directamente en la lista,
para agilizar la gestión de mi inventario.

## Criterios de Aceptación (Gherkin)

```gherkin
Feature: Edición rápida de cantidad
  Scenario: Modificar cantidad con botones
    Given que visualizo la lista de productos
    When pulso el botón + o - junto a un producto
    Then la cantidad se incrementa o disminuye instantáneamente
    And no se permiten cantidades negativas
```

## Notas técnicas
- Actualización instantánea en la UI y backend.

## Desglose Técnico y Estimación de Tareas

- Frontend (FE): S
- Backend (BE): S
- QA: S
