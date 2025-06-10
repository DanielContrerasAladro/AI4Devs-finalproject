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

---

> Prioridad alta en el roadmap tras reunión de planificación 2024-07-17. Esta HU se abordará antes que otras funcionalidades, reservando además un 20% del tiempo de sprint para revisión de bugs y corrección de funcionalidad actual.

## Tareas técnicas / Tickets

- [ ] **BE**: Endpoint `/api/lista/autorrelleno` para obtener lista de la compra autorrellenada según inventario y hábitos
- [ ] **BE**: Lógica de detección de productos faltantes (servicio)
- [ ] **FE**: UI para mostrar y editar la lista autorrellenada
- [ ] **QA**: Casos de prueba para criterios de aceptación
- [ ] **PO**: Validación funcionalidad

### Tabla de responsables y fechas objetivo

| Tarea                                    | Responsable         | Fecha objetivo  |
|------------------------------------------|---------------------|-----------------|
| Endpoint autorrelleno lista (BE)         | BE_Autorrelleno     | 2024-07-22      |
| Lógica productos faltantes (BE)          | BE_Autorrelleno     | 2024-07-22      |
| UI lista autorrellenada (FE)             | FE_Autorrelleno     | 2024-07-24      |
| Casos de prueba QA                       | QA_Autorrelleno     | 2024-07-25      |
| Validación funcionalidad (PO)            | PO_Autorrelleno     | 2024-07-26      |
