# Historia de Usuario: Gestión de iconos y categorías en productos

Como usuario,
quiero poder asignar iconos y categorías a los productos,
para identificarlos visualmente y organizarlos mejor.

## Criterios de Aceptación (Gherkin)

```gherkin
Feature: Iconos y categorías en productos
  Scenario: Asignar icono y categoría
    Given que añado o edito un producto
    Then puedo seleccionar un icono y una categoría de una lista predefinida
    And puedo crear nuevas categorías personalizadas
```

## Notas técnicas
- Lista de iconos predefinidos.
- Categorías editables por el usuario.

## Desglose Técnico y Estimación de Tareas

- Frontend (FE): S
- Backend (BE): S
- QA: S

---

## [2024-07-17] Cierre de historia

La HU_15 ha sido completada, validada y desplegada en producción como parte del hito de internacionalización y robustez del bloque @lists. Todos los criterios de aceptación han sido cubiertos y la funcionalidad está disponible para los usuarios finales.
