# Registro de Bugs y Correcciones

Este documento sirve para registrar y hacer seguimiento de bugs, incidencias y correcciones necesarias, organizadas por página y por agente. Rellena cada apartado con los bugs detectados y su estado.

---

## Páginas principales

### 1. Autenticación
- **Bugs detectados:**
  - [ ] La página inicial debe ser /lists en lugar de / al hacer login
- **Correcciones propuestas:**
  - [ ] Redirigir a /lists cuando el login sea correcto, revisar el funcionamiento y realizar las correcciones oportunas

### 2. Inventario
- **Bugs detectados:**
  - [ ] El módulo para poder añadir un elemento, en lugar de estar en la raíz, debe estar en /lists
- **Correcciones propuestas:**
  - [ ] Mover el módulo de página, revisar el funcionamiento y realizar las correcciones oportunas

### 3. Productos
- **Bugs detectados:**
  - [ ] Añadir un nuevo elemento no está cargando las listas en el seleccionable
  - [ ] No funciona la selección de ícono para la categoría, al pulsar en el ícono debe mostrarse el modal de iconos para seleccionar
  - [ ] Hay que tener cuidado para que las modales se muestren siempre con un z-index superior al del módulo que la llama para poder operar en ella
  - [ ] Debe de poder ser fácil añadir o eliminar la cantidad de un elemento n una lista, con botones '+' y '-' en el listado, al lado del botón para eliminar ese producto de la lista
- **Correcciones propuestas:**
  - [ ] Revisar el funcionamiento y realizar las correcciones oportunas

### 4. Listas de la compra
- **Bugs detectados:**
  - [ ] La lista de la compra debe existir siempre para un usuario, y debe ser la primera seleccionada en la pantalla de listas
  - [ ] Quitar las coletillas IA de cualquier botón de la aplicación
- **Correcciones propuestas:**
  - [ ] Revisar el funcionamiento y realizar las correcciones oportunas

### 5. Menús
- **Bugs detectados:**
  - [ ] Hay un error en MenuState que debe corregirse (Error: 'MenusState' object has no attribute 'get_user_id'red)
  - [ ] El botón 'Generar menú semanal' parece que no hace nada, debería llamar al agente correspondiente con los datos de la aplicación y actualizar el menú semanal, en base a los elementos que tiene el usuario en sus listas
- **Correcciones propuestas:**
  - [ ] Revisar el funcionamiento y realizar las correcciones oportunas

### 6. Recetas
- **Bugs detectados:**
  - [ ] La pantalla debería mostrar un listado de las recetas guardadas por el usuario para poder verlas y editarlas
  - [ ] El botón 'Sugerir receta' muestra el error (Error: 'RecipesState' object has no attribute 'get_user_id'red) cuando debería comunicar con el agente correspondiente y mostrar una receta en base a los elementos que tiene el usuario en sus listas
  - [ ] El botón 'Añadir ingredientes faltantes a la lista de la compra' muestra el siguiente mensaje (Ingredientes añadidos a la lista de la compra.green) pero realmente no hace nada
- **Correcciones propuestas:**
  - [ ] Revisar el funcionamiento y realizar las correcciones oportunas

### 7. Internacionalización
- **Bugs detectados:**
  - [ ] Hay términos en todas las pantallas que no se ven correctamente
- **Correcciones propuestas:**
  - [ ] Revisar el funcionamiento y realizar las correcciones oportunas

### 8. PWA
- **Bugs detectados:**
  - [ ] El login debe almacenarse para intentar hacer login primero ocn ese token, si el token está caducado, volver a recuperarlo de forma transparente al usuario
  - [ ] La aplicación debe ser una PWA, es decir, se debe poder instalar en dispositivos móviles como una aplicación si el dispositivo o SO lo permite
- **Correcciones propuestas:**
  - [ ] Revisar el funcionamiento y realizar las correcciones oportunas

### 9. Componentes y UI
- **Bugs detectados:**
  - [ ] La pantalla del orquestador no se ve igual que el resto de pantallas, se ve más ancha
- **Correcciones propuestas:**
  - [ ] Revisar el funcionamiento y realizar las correcciones oportunas

---

## Agentes y Orquestador IA

### 1. Orquestador IA
- **Bugs detectados:**
  - [ ] Al pulsar el botón que lo llama en la página /orquestador, muestra el error 'Debes iniciar sesión para usar el chat IA.' al pulsar el botón cuando debería comunicar con el orquestador con el mensaje escrito por el usuario y escribir la respuesta a continuación
- **Correcciones propuestas:**
  - [ ]

### 2. Agente IA Nutricional
- **Bugs detectados:**
  - [ ]  Al pulsar el botón que lo llama en la página /lists, muestra el error 'Debes iniciar sesión para usar el chat IA.' al pulsar el botón cuando debería comunicar con el correspondiente agente y añadir el menú a la base de datos del usuario, en base a los elementos que tiene el usuario en sus listas
- **Correcciones propuestas:**
  - [ ] Revisar el funcionamiento y realizar las correcciones oportunas

### 3. Agente IA de Hábitos
- **Bugs detectados:**
  - [ ]  Al pulsar el botón que lo llama en la página /lists, muestra el error 'Debes iniciar sesión para usar el chat IA.' al pulsar el botón cuando debería comunicar con el correspondiente agente y mostrar un informe a continuación en base a los elementos que tiene el usuario en sus listas y a los menús y recetas que se han ido registrando en la base de datos del usuario
- **Correcciones propuestas:**
  - [ ] Revisar el funcionamiento y realizar las correcciones oportunas

### 4. Agente IA Inventario/Alertas
- **Bugs detectados:**
  - [ ]  Al pulsar el botón que lo llama en la página /lists, muestra el error 'Debes iniciar sesión para usar el chat IA.' al pulsar el botón cuando debería comunicar con el correspondiente agente y añadir lo que falte en la lista de la compra, revisando el resto de listas del usuario y klas recetas de los platos registrados en el menú
- **Correcciones propuestas:**
  - [ ] Revisar el funcionamiento y realizar las correcciones oportunas

### 5. LLM Loader / MCP
- **Bugs detectados:**
  - [ ] No parece que sea llamado en ningún momento
- **Correcciones propuestas:**
  - [ ] Revisar el funcionamiento y realizar las correcciones oportunas

---
