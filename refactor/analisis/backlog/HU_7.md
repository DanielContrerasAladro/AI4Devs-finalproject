Título de la Historia de Usuario:
Recomendaciones de IA para menús

Como usuario autenticado,
quiero recibir recomendaciones de menús saludables basadas en los productos de mi alacena,
para que pueda planificar mis comidas de forma equilibrada y aprovechar mejor mis alimentos.

Criterios de Aceptación:
- El sistema sugiere menús diarios o semanales en función del inventario disponible.
- Las recomendaciones consideran preferencias y restricciones alimentarias del usuario.
- El usuario puede aceptar, rechazar o modificar las sugerencias.
- El sistema explica brevemente el motivo de cada recomendación.

Notas Adicionales:
- El agente IA debe aprender de las elecciones del usuario para mejorar futuras sugerencias.
- Las recomendaciones deben ser accesibles desde la pantalla principal o sección de menús.

Historias de Usuario Relacionadas:
- HU_8 (Generación automática de lista de la compra)
- HU_6 (Edición de perfil de usuario)

---

## Desglose Técnico y Estimación de Tickets

### Frontend (Python (PyScript/Anvil))
- Implementar interfaz para mostrar recomendaciones de menús
  _Talla de camiseta: M_
- Permitir aceptar, rechazar o modificar sugerencias
  _Talla de camiseta: S_
- Visualizar explicación de la recomendación
  _Talla de camiseta: S_
- Integración con API de IA de menús
  _Talla de camiseta: S_

### Backend (FastAPI + IA)
- Endpoint para obtener recomendaciones de menús (GET /menus/recomendaciones)
  _Talla de camiseta: L_
- Lógica de IA para sugerir menús según inventario y preferencias
  _Talla de camiseta: L_
- Registro de feedback del usuario para aprendizaje automático
  _Talla de camiseta: M_

### QA/Testing
- Pruebas unitarias y de integración para recomendaciones de menús
  _Talla de camiseta: M_

---

```mermaid
graph TD
    FE1[Mostrar recomendaciones] --> FE2[Aceptar/rechazar/modificar]
    FE2 --> FE3[Visualizar explicación]
    FE3 --> FE4[Integración API IA]
    BE1[Obtener recomendaciones] --> BE2[Lógica IA menús]
    BE2 --> BE3[Registro feedback]
    FE4 --> QA1[Pruebas recomendaciones]
    BE3 --> QA1
