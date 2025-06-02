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

---

## [2024-07-17] Cierre de historia

La HU_18 ha sido completada, validada y desplegada en producción como parte del hito de internacionalización y robustez del bloque @lists. Todos los criterios de aceptación han sido cubiertos y la funcionalidad está disponible para los usuarios finales.
