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

---

> Prioridad alta en el roadmap tras reunión de planificación 2024-07-17. Esta HU se abordará antes que otras funcionalidades, reservando además un 20% del tiempo de sprint para revisión de bugs y corrección de funcionalidad actual.

## Tareas técnicas / Tickets

- [ ] **BE**: Endpoint `/api/recetas/ia` para sugerir recetas usando IA
- [ ] **BE**: Lógica para añadir ingredientes faltantes a la lista de la compra
- [ ] **FE**: UI para selección de recetas IA y gestión de lista
- [ ] **QA**: Casos de prueba para criterios de aceptación
- [ ] **PO**: Validación funcionalidad

### Tabla de responsables y fechas objetivo

| Tarea                                    | Responsable         | Fecha objetivo  |
|------------------------------------------|---------------------|-----------------|
| Endpoint recetas IA (BE)                 | BE_IARecetas        | 2024-07-22      |
| Lógica añadir ingredientes (BE)          | BE_IARecetas        | 2024-07-22      |
| UI selección recetas IA (FE)             | FE_IARecetas        | 2024-07-24      |
| Casos de prueba QA                       | QA_IARecetas        | 2024-07-25      |
| Validación funcionalidad (PO)            | PO_IARecetas        | 2024-07-26      |
