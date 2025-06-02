# Historia de Usuario: Listas personalizables y compartibles

Como usuario,
quiero poder crear, personalizar y compartir listas de la compra,
para organizar mis compras y colaborar con otras personas.

## Criterios de Aceptación (Gherkin)

```gherkin
Feature: Listas personalizables y compartibles
  Scenario: Crear y personalizar lista
    Given que accedo a la sección de listas
    When creo una nueva lista
    Then puedo ponerle nombre, color y descripción

  Scenario: Compartir lista
    Given que tengo una lista creada
    When selecciono la opción de compartir
    Then puedo invitar a otros usuarios a colaborar en la lista
```

## Notas técnicas
- Compartición por email o enlace.
- Personalización visual mínima (nombre, color, icono opcional).

## Desglose Técnico y Estimación de Tareas

- Frontend (FE): M
- Backend (BE): M
- QA: S

---

## [2024-07-17] Cierre de historia

La HU_14 ha sido completada, validada y desplegada en producción como parte del hito de internacionalización y robustez del bloque @lists. Todos los criterios de aceptación han sido cubiertos y la funcionalidad está disponible para los usuarios finales.
