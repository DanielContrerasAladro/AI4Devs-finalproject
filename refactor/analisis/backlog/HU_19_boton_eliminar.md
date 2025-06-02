# Historia de Usuario: Botón de eliminar producto visible

Como usuario,
quiero que el botón para eliminar productos sea visible y accesible en la lista,
para poder borrar productos fácilmente cuando lo necesite.

## Criterios de Aceptación (Gherkin)

```gherkin
Feature: Botón de eliminar producto
  Scenario: Eliminar producto desde la lista
    Given que visualizo la lista de productos
    When pulso el botón de eliminar junto a un producto
    Then el producto se elimina tras confirmación
```

## Notas técnicas
- Confirmación antes de eliminar.
- Botón visible en cada fila de producto.

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

---

## [2024-07-17] Cierre de historia

La HU_19 ha sido completada, validada y desplegada en producción como parte del hito de internacionalización y robustez del bloque @lists. Todos los criterios de aceptación han sido cubiertos y la funcionalidad está disponible para los usuarios finales.
