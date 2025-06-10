# Historia de Usuario: Menús semanales con IA y comidas fuera

Como usuario,
quiero planificar menús semanales con ayuda de IA e indicar los días que como fuera,
para organizar mejor mis comidas y compras.

## Criterios de Aceptación (Gherkin)

```gherkin
Feature: Menús semanales con IA y comidas fuera
  Scenario: Planificación de menú semanal
    Given que accedo a la sección de menús
    When planifico la semana
    Then puedo marcar los días que como fuera y recibir sugerencias de menús de IA para el resto
```

## Notas técnicas
- Integración con IA y gestión visual de calendario.

## Desglose Técnico y Estimación de Tareas

- Frontend (FE): M
- Backend (BE): M
- QA: S

| Rol  | Responsable | Observaciones |
|------|-------------|--------------|
| FE   | FE_MenusIA   |              |
| BE   | BE_MenusIA   |              |
| QA   | QA_MenusIA   |              |
| PO   | PO_MenusIA   | Validación de criterios de aceptación |
| BA   | BA_MenusIA   | Validación de requisitos y coherencia |

## QA/PO: Criterios de aceptación y pruebas

- QA: Preparar casos de prueba para cada criterio de aceptación.
- PO: Validar que la funcionalidad cumple los criterios definidos.
- QA: Documentar resultados de pruebas y feedback.

---

> Prioridad alta en el roadmap tras reunión de planificación 2024-07-17. Esta HU se abordará antes que otras funcionalidades, reservando además un 20% del tiempo de sprint para revisión de bugs y corrección de funcionalidad actual.

## Tareas técnicas / Tickets

- [ ] **BE**: Endpoint `/api/menus/ia` para sugerir menús semanales usando IA
- [ ] **BE**: Lógica para marcar días fuera y personalizar menú
- [ ] **FE**: UI para planificación semanal y selección de días fuera
- [ ] **QA**: Casos de prueba para criterios de aceptación
- [ ] **PO**: Validación funcionalidad

### Tabla de responsables y fechas objetivo

| Tarea                                    | Responsable         | Fecha objetivo  |
|------------------------------------------|---------------------|-----------------|
| Endpoint menús IA (BE)                   | BE_MenusIA          | 2024-07-22      |
| Lógica días fuera (BE)                   | BE_MenusIA          | 2024-07-22      |
| UI planificación semanal (FE)            | FE_MenusIA          | 2024-07-24      |
| Casos de prueba QA                       | QA_MenusIA          | 2024-07-25      |
| Validación funcionalidad (PO)            | PO_MenusIA          | 2024-07-26      |
