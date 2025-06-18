# Historia de Usuario: Selector de idioma y estilo personalizable

Como usuario,
quiero poder elegir el idioma y el estilo visual de la app,
para adaptarla a mis preferencias y necesidades.

## Criterios de Aceptación (Gherkin)

```gherkin
Feature: Selector de idioma y estilo
  Scenario: Cambiar idioma
    Given que accedo a la configuración
    When selecciono un idioma distinto
    Then toda la app se muestra en el idioma elegido

  Scenario: Cambiar estilo visual
    Given que accedo a la configuración
    When selecciono un tema visual
    Then la app cambia su apariencia según el tema elegido
```

## Estado actual

- [x] Corrección de traducciones completada
- [x] Archivos de i18n revisados y actualizados
- [ ] Pendiente validar funcionamiento en producción en Reflex Hosting
- [ ] Pendiente implementar selector de tema visual

## Desglose Técnico y Estimación de Tareas

- Frontend (FE): M
- Backend (BE): S
- QA: S

| Rol  | Responsable | Estado |
|------|-------------|---------|
| FE   | FE_Internacionalización   | En progreso |
| BE   | BE_Internacionalización   | Completado |
| QA   | QA_Internacionalización   | En progreso |
| PO   | PO_Internacionalización   | En revisión |
| BA   | BA_Internacionalización   | En revisión |

## QA/PO: Criterios de aceptación y pruebas

- [x] QA: Casos de prueba para traducciones completados
- [x] PO: Traducciones validadas y correctas
- [ ] QA: Pendiente validar selector de tema visual

---

> [2024-07-18] Actualización: Corrección de traducciones completada y desplegada. Pendiente validar funcionamiento en producción y completar selector de tema visual.

# Historia de Usuario: Corrección bug i18n en producción

Como desarrollador,
quiero que los archivos de i18n se suban y sirvan correctamente en producción,
para que el selector de idioma funcione en Reflex Hosting.

## Criterios de Aceptación (Gherkin)

```gherkin
Feature: Bug i18n en producción
  Scenario: Despliegue de archivos de idioma
    Given que despliego la app en Reflex Hosting
    Then los archivos de i18n están accesibles y el selector de idioma funciona correctamente
```

## Desglose Técnico y Estimación de Tareas

- Frontend (FE): M
- Backend (BE): S
- QA: S

| Rol  | Responsable | Observaciones |
|------|-------------|--------------|
| FE   | FE_Internacionalización   |              |
| BE   | BE_Internacionalización   |              |
| QA   | QA_Internacionalización   |              |
| PO   | PO_Internacionalización   | Validación de criterios de aceptación |
| BA   | BA_Internacionalización   | Validación de requisitos y coherencia |

## QA/PO: Criterios de aceptación y pruebas

- QA: Preparar casos de prueba para cada criterio de aceptación.
- PO: Validar que la funcionalidad cumple los criterios definidos.
- QA: Documentar resultados de pruebas y feedback.
