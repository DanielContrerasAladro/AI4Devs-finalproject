# Historia de Usuario: Logado permanente (auto-login)

Como usuario,
quiero que mi sesión permanezca activa aunque cierre la app,
para no tener que iniciar sesión cada vez que la abro.

## Criterios de Aceptación (Gherkin)

```gherkin
Feature: Logado permanente
  Scenario: Auto-login al abrir la app
    Given que he iniciado sesión previamente
    When abro la app de nuevo
    Then accedo directamente sin tener que volver a logarme
```

## Notas técnicas
- Uso de tokens persistentes y refresco automático.

## Desglose Técnico y Estimación de Tareas

- Frontend (FE): S
- Backend (BE): S
- QA: S

| Rol  | Responsable | Observaciones |
|------|-------------|--------------|
| FE   | FE_Auth   |              |
| BE   | BE_Auth   |              |
| QA   | QA_Auth   |              |
| PO   | PO_Auth   | Validación de criterios de aceptación |
| BA   | BA_Auth   | Validación de requisitos y coherencia |

## QA/PO: Criterios de aceptación y pruebas

- QA: Preparar casos de prueba para cada criterio de aceptación.
- PO: Validar que la funcionalidad cumple los criterios definidos.
- QA: Documentar resultados de pruebas y feedback.

---

> Prioridad alta en el roadmap tras reunión de planificación 2024-07-17. Esta HU se abordará tras las funcionalidades de IA y PWA, reservando además un 20% del tiempo de sprint para revisión de bugs y corrección de funcionalidad actual.

## Estado actual

- [ ] Implementación pendiente tras bloque de IA y PWA.
- [x] Lógica de autenticación y persistencia de sesión revisada y mejorada en el refactor reciente.
- [ ] Validación final y QA tras despliegue de nuevas funcionalidades.

> Última actualización: 2024-07-18. Refleja avances en la gestión de sesión y autenticación tras refactor global.
