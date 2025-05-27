## Índice

0. [Ficha del proyecto](#0-ficha-del-proyecto)
1. [Descripción general del producto](#1-descripción-general-del-producto)
2. [Arquitectura del sistema](#2-arquitectura-del-sistema)
3. [Modelo de datos](#3-modelo-de-datos)
4. [Especificación de la API](#4-especificación-de-la-api)
5. [Historias de usuario](#5-historias-de-usuario)
6. [Pull requests](#6-pull-requests)

---

## 0. Ficha del proyecto

### **0.1. Tu nombre completo:**

> Daniel Contreras Aladro

### **0.2. Nombre del proyecto:**

> Alacena

### **0.3. Descripción breve del proyecto:**

> Alacena es una aplicación móvil diseñada para ayudar a los usuarios a organizar su despensa de manera eficiente, utilizando tecnologías modernas como Angular, Ionic y Firebase para ofrecer una experiencia de usuario fluida y moderna.
> El objetivo del proyecto es realizar una refactorización del proyecto, renovando el código del proyecto a las últimas versiones de las tecnologías utilizadas o modificar las tecnologías actualizadas para adaptarlo a las nuevas necesidades.
> En el proyecto se va a obviar la parte de applicación móvil y se reconvertirá en una PWA, manteniendo toda la funcionalidad
> A la funcionalidad se intentará añadir un agente IA experto en nutrición saludable que ayude en la elección de menús, realización de lista de la compra y demás acciones que deban realizarse automáticamente según el uso de cada usuario
> Se ha escrito una [propuesta de refactorización](propuesta_refactorizacion.md) del proyecto en base a estas necesidades.
> También se ha definido un [Documento de Requisitos del Producto (PRD)](analisis/prd.md) que detalla los objetivos y funcionalidades del proyecto.

### **0.4. URL del proyecto:**

> [Blog promocional](https://chonyfrikadas.blogspot.com/2016/03/alacena-tu-nueva-app-para-gestion.html)

> [Alacena en producción](https://frontend-navy-grass.reflex.run/)

### 0.5. URL o archivo comprimido del repositorio

> [Repositorio final project](https://github.com/DanielContrerasAladro/AI4Devs-finalproject)

> [Repositorio Alacena](https://github.com/DanielContrerasAladro/Alacena)


---

## 1. Descripción general del producto

### **1.1. Objetivo:**

> **Alacena** tiene como objetivo principal facilitar la gestión integral de la despensa y la alimentación saludable de los usuarios, a través de una aplicación web progresiva (PWA) moderna, accesible y multiplataforma.
>
> **Objetivos específicos:**
>
> - **Organización eficiente de la despensa:**
>   Permitir a los usuarios registrar, clasificar y consultar los alimentos disponibles en casa, con información sobre cantidades, fechas de caducidad y categorías.
>
> - **Planificación de menús saludables:**
>   Integrar un agente de inteligencia artificial experto en nutrición que sugiera menús semanales personalizados, adaptados a las necesidades, preferencias y restricciones alimentarias del usuario, así como a los ingredientes disponibles.
>
> - **Gestión automatizada de la lista de la compra:**
>   Generar automáticamente la lista de la compra en función de los menús planificados y el inventario actual, permitiendo añadir, eliminar o compartir productos fácilmente.
>
> - **Funcionalidad offline y sincronización en la nube:**
>   Garantizar el acceso y la edición de los datos sin conexión, sincronizando los cambios cuando haya acceso a internet y permitiendo el login seguro (incluyendo opciones sociales como Google o Apple).
>
> - **Notificaciones inteligentes:**
>   Avisar al usuario sobre productos próximos a agotarse o caducar, y sobre necesidades de compra para completar recetas o menús.
>
> - **Diseño inclusivo y adaptable:**
>   Ofrecer una experiencia de usuario intuitiva, accesible, responsive y multilingüe, compatible con diferentes dispositivos, navegadores y resoluciones.
>
> - **Colaboración y compartición:**
>   Permitir compartir listas de la compra y recetas con otros usuarios, facilitando la gestión familiar o en grupo.
>
> - **Automatización y personalización:**
>   Adaptar las recomendaciones y funcionalidades a los hábitos y preferencias del usuario, permitiendo registrar eventos como comidas fuera de casa.
>
> - **Calidad y mantenibilidad:**
>   Aplicar buenas prácticas de desarrollo (TDD, CI/CD) para asegurar la calidad, facilidad de despliegue y evolución del producto.

### **1.2. Características y funcionalidades principales:**

> #### 1. Quiero poder añadir, eliminar y clasificar los alimentos de mi despensa, ver fácilmente qué tengo, en qué cantidad y cuándo caducan.
>
> - Gestión de inventario de despensa: permite añadir y eliminar artículos.
> - Gestionar los alimentos que tenemos en casa, saber qué tenemos y qué falta para poder hacer la compra.
> - Poder añadir y gestionar ingredientes, de manera que podamos saber qué alimentos tenemos en casa y qué falta para poder hacer una receta.
> - Poder añadir y gestionar categorías, de manera que podamos clasificar los alimentos y las recetas.
> - Poder añadir y gestionar unidades de medida, de manera que podamos saber qué cantidad de alimentos tenemos en casa y qué falta para poder hacer una receta. (gramos, kilos, litros, etc.)
> - Recibir notificaciones y gestionar las fechas de caducidad de los alimentos (por ejemplo, si un alimento caduca en 3 días, recibir una notificación para que lo consumamos antes de que caduque); que la fecha de caducidad sea configurable por el usuario.
>
> #### 2. Me gustaría que la aplicación me ayude a planificar menús saludables adaptados a mis necesidades, preferencias y a los ingredientes que ya tengo en casa.
>
> - Generación de menús saludables personalizados según las necesidades y preferencias del usuario.
> - Añadir un agente de IA que nos ayude a gestionar los alimentos y las recetas, de manera que podamos saber qué alimentos tenemos en casa y qué falta para poder hacer una receta.
> - Añadir conocimientos de alimentación saludable al agente de IA, de manera que nos pueda recomendar recetas saludables y nos pueda ayudar a gestionar los alimentos de manera saludable.
>
> #### 3. Quiero que se genere automáticamente mi lista de la compra según los menús y lo que me falta en la despensa, y poder añadir o quitar productos fácilmente.
>
> - Gestión de la lista de compras basada en el menú semanal o preferencias del usuario.
> - Poder añadir alimentos a la lista de la compra, incluso que la aplicación lo haga de forma automática.
>
> #### 4. Necesito poder guardar y consultar recetas, ver qué ingredientes necesito y vincularlos con mi inventario y lista de la compra.
>
> - Poder añadir y gestionar recetas, de manera que podamos saber qué alimentos necesitamos para hacer una receta.
> - Poder añadir y gestionar ingredientes, de manera que podamos saber qué alimentos tenemos en casa y qué falta para poder hacer una receta.
>
> #### 5. Me gustaría poder organizar mis alimentos y recetas usando etiquetas y categorías personalizables.
>
> - Poder añadir y gestionar etiquetas, de manera que podamos clasificar los alimentos y las recetas.
> - Poder añadir y gestionar categorías, de manera que podamos clasificar los alimentos y las recetas.
>
> #### 6. Quiero recibir notificaciones cuando un alimento esté a punto de agotarse o caducar, o si me falta algo para una receta o menú.
>
> - Notificaciones de artículos por agotarse.
> - Recibir notificaciones cuando se acabe un alimento o cuando falte un alimento para poder hacer una receta.
> - Recibir notificaciones y gestionar las fechas de caducidad de los alimentos (por ejemplo, si un alimento caduca en 3 días, recibir una notificación para que lo consumamos antes de que caduque); que la fecha de caducidad sea configurable por el usuario.
>
> #### 7. Necesito que la aplicación funcione aunque no tenga conexión a internet, y que se sincronice automáticamente cuando vuelva a estar conectado.
>
> - Funcionalidad offline y online.
> - Sincronización de datos entre dispositivos.
>
> #### 8. Quiero poder iniciar sesión de forma segura, usando mi cuenta de Google o Apple, y acceder a mis datos desde cualquier dispositivo.
>
> - Poder hacer login social, Google o Apple, de manera que podamos compartir las listas de la compra con otros usuarios.
>
> #### 9. Me gustaría compartir mis listas de la compra y recetas con mi familia o amigos para organizar la compra y la cocina en grupo.
>
> - Poder compartir las listas de la compra con otros usuarios.
>
> #### 10. Quiero que la aplicación aprenda de mis hábitos y preferencias, y que pueda registrar si he comido fuera o si cambio algún menú.
>
> - Añadir un agente de IA que nos ayude a gestionar los alimentos y las recetas, de manera que podamos saber qué alimentos tenemos en casa y qué falta para poder hacer una receta.
> - Añadir conocimientos de alimentación saludable al agente de IA, de manera que nos pueda recomendar recetas saludables y nos pueda ayudar a gestionar los alimentos de manera saludable.
>
> #### 11. Necesito que la interfaz sea fácil de usar, moderna, accesible, y que funcione bien en cualquier dispositivo, navegador, idioma o tamaño de pantalla.
>
> - Interfaz de usuario intuitiva y moderna.
> - Soporte multilingüe y adaptabilidad a diferentes navegadores y resoluciones.
>
> #### 12. Quiero confiar en que la aplicación es robusta, se actualiza fácilmente y mantiene mis datos seguros.
>
> - Sincronización de datos entre dispositivos.
> - Funcionalidad offline y online.

### **1.3. Diseño y experiencia de usuario:**

> Alacena ofrece un diseño limpio y moderno, adaptado a diferentes tamaños de pantalla y resoluciones, asegurando una experiencia de usuario accesible y responsiva. El diseño es inclusivo, permitiendo su uso en diferentes idiomas y asegurando la accesibilidad para todos los usuarios.
> Partiendo de la URL del proyecto, proporciona capturas de pantalla y/o wireframes que muestren el diseño y la experiencia de usuario de la aplicación.
> Debe tener una interfaz intuitiva y fácil de usar, de manera que el usuario pueda gestionar los alimentos y las recetas de manera sencilla y rápida.
> Se puede ver el funcionamiento y una explicación actual [aquí](#04-url-del-proyecto).

### **1.4. Instrucciones de instalación:(actuales)**
> - Clonar el repositorio desde la URL proporcionada.
> - Instalar las dependencias necesarias utilizando `npm install`.
> - Configurar Firebase con las credenciales adecuadas.
> - Ejecutar la aplicación con `ionic serve` para desarrollo local.

---

## 2. Arquitectura del Sistema

### **2.1. Diagrama de arquitectura:**
### **2.1.1 (actual)**
> ```mermaid
> flowchart TD
>     subgraph Cliente [Aplicación Móvil Ionic + Angular]
>         UI[Interfaz de Usuario]
>         Logic[Lógica de Negocio Angular Services]
>         Notif[Notificaciones Locales]
>     end
>
>     subgraph Servidor [Firebase]
>         Auth[Autenticación Firebase Auth]
>         DB[Base de Datos en Tiempo Real Realtime Database]
>         Storage[Almacenamiento de Archivos]
>         FCM[Notificaciones Push Firebase Cloud Messaging]
>     end
>
>     UI --> Logic
>     Logic -->|Lectura/Escritura| DB
>     Logic -->|Gestión de usuarios| Auth
>     Logic -->|Subida/Descarga| Storage
>     Logic -->|Envío/Recepción| Notif
>     Notif -->|Sincronización| FCM
>     FCM -->|Push| Notif
>
>     DB <--> Auth
>     DB <--> Storage
>
>     %% Sincronización entre dispositivos
>     DB -- Sincronización en tiempo real --> Logic
>
>     %% Seguridad
>     Auth -- Permisos y Seguridad --> DB
>
>     %% Despliegue
>     subgraph Despliegue
>         FirebaseHosting[Firebase Hosting Web]
>         AppStores[App Stores iOS/Android]
>     end
>     Cliente -->|Distribución| AppStores
>     Servidor -->|Web| FirebaseHosting
> ```
>
> ### Explicación
>
> - **Cliente**: La app móvil desarrollada con Ionic y Angular, que incluye la interfaz de usuario, lógica de negocio y notificaciones locales.
> - **Servidor (Firebase)**: Provee autenticación, base de datos en tiempo real, almacenamiento y notificaciones push.
> - **Comunicación**: El cliente interactúa con Firebase para autenticación, gestión de datos y archivos, y recibe notificaciones tanto locales como push.
> - **Sincronización**: Los datos se sincronizan en tiempo real entre dispositivos a través de la base de datos de Firebase.
> - **Seguridad**: La autenticación controla el acceso y los permisos sobre los datos.
> - **Despliegue**: La app se distribuye vía App Stores y la versión web mediante Firebase Hosting.
> Usa el formato que consideres más adecuado para representar los componentes principales de la aplicación y las tecnologías utilizadas. Explica si sigue algún patrón predefinido, justifica por qué se ha elegido esta arquitectura, y destaca los beneficios principales que aportan al proyecto y justifican su uso, así como sacrificios o déficits que implica.

### **2.1.2 (objetivo)**
> ```mermaid
> flowchart TD
>     subgraph Cliente [PWA PyScript/Anvil]
>         UI[UI/UX TailwindCSS + Python]
>         Logic[Lógica de Negocio Python]
>         SW[Service Worker Offline]
>         IA[Agente IA API Python]
>     end
>
>     subgraph Backend [Supabase Hosting]
>         Auth[Auth OAuth, Email, Social]
>         DB[PostgreSQL DB + JSONB]
>         Storage[Storage]
>         Edge[Edge Functions]
>         Realtime[Realtime]
>     end
>
>     UI --> Logic
>     Logic -->|Lectura/Escritura| DB
>     Logic -->|Gestión de usuarios| Auth
>     Logic -->|Subida/Descarga| Storage
>     Logic -->|Realtime| Realtime
>     Logic -->|Lógica avanzada| Edge
>     Logic -->|Recomendaciones| IA
>     SW -->|Sincronización| DB
>
>     Cliente -->|Web| Supabase
>     IA -->|API| Backend
> ```

> ### Explicación
>
> - **Cliente (PWA con PyScript/Anvil)**: La aplicación pasa a ser una PWA moderna, desarrollada con tecnologías como PyScript o Anvil, lo que permite ejecutar lógica de negocio en Python directamente en el navegador. Incluye una interfaz de usuario moderna (UI/UX) basada en TailwindCSS y Python, un Service Worker para funcionalidad offline y sincronización, y un agente de IA especializado en nutrición saludable que asiste en la planificación de menús y la gestión de la despensa.
> - **Backend (Supabase)**: Se utiliza Supabase como backend, proporcionando autenticación segura (OAuth, email, social), base de datos relacional (PostgreSQL con soporte para JSONB), almacenamiento de archivos, funciones edge para lógica avanzada y capacidades de sincronización en tiempo real.
> - **Comunicación**: El cliente interactúa con Supabase para autenticación, gestión de datos, almacenamiento y lógica avanzada mediante edge functions. El agente de IA se comunica mediante API para ofrecer recomendaciones personalizadas. El Service Worker garantiza la funcionalidad offline y la sincronización de datos cuando hay conexión.
> - **Sincronización y Offline**: Gracias al Service Worker y las capacidades de Supabase, la aplicación permite trabajar sin conexión y sincroniza los cambios automáticamente cuando se recupera la conectividad.
> - **Seguridad**: La autenticación y los permisos se gestionan a través de Supabase, asegurando el acceso seguro a los datos y funcionalidades.
> - **Despliegue**: La aplicación se despliega como PWA a través de Supabase Hosting, eliminando la dependencia de las tiendas de aplicaciones tradicionales y facilitando actualizaciones continuas.

> **Beneficios principales:**
> - Modernización tecnológica y mayor flexibilidad gracias a Python en frontend y backend.
> - Mejor experiencia de usuario con PWA, funcionalidad offline y sincronización automática.
> - Integración nativa de IA para recomendaciones personalizadas.
> - Despliegue y mantenimiento simplificados.

> **Sacrificios o déficits:**
> - Requiere adaptación de los usuarios a la nueva experiencia PWA.
> - Dependencia de tecnologías emergentes (PyScript/Anvil) que pueden tener menor madurez o soporte que frameworks tradicionales.
> - Migración de datos y lógica desde Firebase a Supabase y Python.

### **2.2. Descripción de componentes principales:**

> A continuación se describen los componentes principales del sistema, indicando la tecnología utilizada en la situación actual y la tecnología objetivo tras la refactorización:
>
> - **Frontend / Interfaz de Usuario**
>   - *Actual*: Angular (TypeScript) + Ionic Framework. Permite el desarrollo de aplicaciones móviles híbridas multiplataforma con una experiencia nativa y componentes UI reutilizables. Ejemplo: uso de `@ionic/angular` para vistas y navegación.
>   - *Objetivo*: PyScript o Anvil (Python) como base para una PWA moderna, con TailwindCSS para el diseño UI/UX. Permite desarrollar la interfaz completamente en Python, facilitando la integración con lógica avanzada y la reutilización de código. [Referencia PyScript](https://pyscript.net/), [Referencia Anvil](https://anvil.works/).
>
> - **Lógica de Negocio**
>   - *Actual*: Servicios de Angular (TypeScript) gestionan la lógica de negocio, comunicación con Firebase y manipulación de datos.
>   - *Objetivo*: Lógica implementada en Python, reutilizable tanto en frontend (PyScript/Anvil) como en microservicios backend. Permite mayor cohesión y reutilización de código entre cliente y servidor.
>
> - **Backend / Base de Datos**
>   - *Actual*: Firebase Realtime Database y Firebase Auth para autenticación y almacenamiento de datos en tiempo real. Ejemplo: reglas de seguridad y sincronización automática entre dispositivos.
>   - *Objetivo*: Supabase (PostgreSQL con soporte JSONB) para almacenamiento estructurado y semiestructurado, autenticación OAuth/social, almacenamiento de archivos y edge functions para lógica avanzada. [Referencia Supabase](https://supabase.com/).
>
> - **Notificaciones y Sincronización**
>   - *Actual*: Firebase Cloud Messaging (FCM) para notificaciones push y sincronización en tiempo real mediante Firebase.
>   - *Objetivo*: Service Worker para funcionalidad offline y sincronización en la PWA, y Supabase Realtime para eventos en tiempo real. Las notificaciones pueden gestionarse mediante APIs web estándar o integraciones externas.
>
> - **Agente IA**
>   - *Actual*: No disponible.
>   - *Objetivo*: Microservicio Python (Flask/FastAPI) integrado con Supabase y consumido desde el frontend, especializado en nutrición saludable y recomendaciones personalizadas. [Ejemplo de integración](https://supabase.com/docs/guides/getting-started/ai-prompts).

### **2.3. Descripción de alto nivel del proyecto y estructura de ficheros**

#### 2.3.1 (actual)

> El proyecto actual está basado en una arquitectura móvil híbrida utilizando Angular, Ionic y Firebase. La estructura de ficheros se organiza en torno a los módulos de Angular, componentes de Ionic y la configuración de Firebase, permitiendo una gestión eficiente de la lógica de negocio, vistas y servicios. Incluye carpetas para componentes, servicios, modelos, assets y configuración específica de la plataforma. El despliegue y la integración con Firebase están presentes en la raíz del proyecto.
> ```md
> Alacena
> |── src
> | |── app
> | |── classes
> | |── providers
> | |── pipes
> | |── components
> | |── theme
> | |── assets
> | |── pages
> | |-- services
> |── firebase
> |── config
> |── node_modules
> |── ionic.config.json
> |── package.json
> |── angular.json
> |── firebase.json
> ```

#### 2.3.2 (objetivo)

> La situación objetivo plantea una PWA moderna y modular, desarrollada principalmente en Python (PyScript/Anvil) y desplegada sobre Supabase. La estructura de carpetas se orienta a la separación clara entre frontend (PWA en Python), microservicio de IA, configuración de Supabase, tests y automatización CI/CD. Esto facilita la escalabilidad, el mantenimiento y la integración continua, permitiendo una evolución ágil del producto.
>
> ```mmd
> Alacena/
> │
> ├── frontend/
> │   ├── components/
> │   │   ├── RegisterForm.py         # Formulario de registro
> │   │   ├── LoginForm.py            # Formulario de login
> │   │   ├── ProductForm.py          # Añadir/editar producto
> │   │   └── ProductList.py          # Listado de inventario
> │   ├── pages/
> │   │   ├── Home.py                 # Página principal (inventario)
> │   │   ├── Register.py             # Página de registro
> │   │   ├── Login.py                # Página de login
> │   │   └── NotFound.py             # Página 404
> │   ├── services/
> │   │   ├── supabase_client.py      # Cliente y helpers de Supabase
> │   │   ├── auth.py                 # Lógica de autenticación
> │   │   └── products.py             # Lógica de productos
> │   ├── assets/
> │   │   └── logo.png
> │   ├── theme/
> │   │   └── tailwind.config.js      # Configuración de TailwindCSS
> │   ├── main.py                     # Entry point de la app
> │   └── README.md
> │
> ├── supabase/
> │   ├── schema.sql                  # Esquema de tablas y RLS
> │   └── seed.sql                    # Datos de ejemplo (opcional)
> │
> ├── tests/
> │   ├── unit/
> │   │   ├── test_auth.py
> │   │   └── test_products.py
> │   ├── integration/
> │   │   └── test_end_to_end.py
> │   └── e2e/
> │       └── test_user_journey.py
> │
> ├── .github/
> │   └── workflows/
> │       └── deploy.yml              # CI/CD para despliegue automático
> │
> ├── requirements.txt                # Dependencias Python (supabase, pyscript, etc.)
> ├── README.md                       # Documentación general del proyecto
> └── CHANGELOG.md                    # Cambios y releases
> ```

### **2.4. Infraestructura y despliegue**

#### 2.4.1 (actual)

> La infraestructura actual se basa en el ecosistema de Firebase, utilizando Firebase Hosting para la web, Firebase Realtime Database y Auth para la gestión de datos y usuarios, y Firebase Cloud Messaging para notificaciones. El desarrollo y despliegue se realiza principalmente con herramientas de Ionic y Angular CLI.
>
> ```mermaid
> flowchart TD
>     Dev[Desarrollador]
>     Git[Repositorio Git]
>     CLI[Ionic/Angular CLI]
>     FirebaseHosting[Firebase Hosting]
>     AppStores[App Stores iOS/Android]
>     App[Aplicación Móvil Ionic/Angular]
>     Auth[Firebase Auth]
>     DB[Firebase Realtime Database]
>     Storage[Firebase Storage]
>     FCM[Firebase Cloud Messaging]
>
>     Dev -->|Push| Git
>     Git -->|CI/CD opcional| CLI
>     CLI -->|Build/Deploy| FirebaseHosting
>     CLI -->|Build| AppStores
>     FirebaseHosting --> App
>     AppStores --> App
>     App --> Auth
>     App --> DB
>     App --> Storage
>     App --> FCM
>     Auth <--> DB
>     DB <--> Storage
> ```
>
> **Despliegue actual:**
> - El desarrollador realiza cambios y los sube al repositorio Git.
> - Se utiliza Ionic/Angular CLI para construir la aplicación y desplegarla en Firebase Hosting (web) o en las tiendas de aplicaciones (iOS/Android).
> - Firebase gestiona la autenticación, base de datos, almacenamiento y notificaciones push.

#### 2.4.2 (objetivo)

> La infraestructura objetivo se apoya en Supabase como backend principal (hosting, base de datos, autenticación, almacenamiento y edge functions), y en una PWA desarrollada en Python (PyScript/Anvil) como frontend. El despliegue y la integración continua se gestionan mediante GitHub Actions.
>
> ```mermaid
> flowchart TD
>     Dev[Desarrollador]
>     Git[Repositorio GitHub]
>     Actions[GitHub Actions CI/CD]
>     SupabaseHosting[Supabase Hosting PWA]
>     PWA[PWA PyScript/Anvil]
>     Auth[Supabase Auth]
>     DB[Supabase PostgreSQL + JSONB]
>     Storage[Supabase Storage]
>     Edge[Supabase Edge Functions]
>     Realtime[Supabase Realtime]
>     IA[Microservicio IA Python]
>
>     Dev -->|Push| Git
>     Git -->|CI/CD| Actions
>     Actions -->|Build/Deploy| SupabaseHosting
>     SupabaseHosting --> PWA
>     PWA --> Auth
>     PWA --> DB
>     PWA --> Storage
>     PWA --> Realtime
>     PWA --> Edge
>     PWA --> IA
>     IA --> DB
>     IA --> Auth
> ```
>
> **Despliegue objetivo:**
> - El desarrollador sube los cambios al repositorio GitHub.
> - GitHub Actions ejecuta los tests y despliega automáticamente la PWA en Supabase Hosting.
> - Supabase gestiona la autenticación, base de datos relacional, almacenamiento, edge functions y eventos en tiempo real.
> - El microservicio de IA se integra mediante API y accede a Supabase para lógica avanzada y recomendaciones.

### **2.5. Seguridad**

> A continuación se enumeran las principales prácticas y elementos de seguridad implementados en el proyecto, diferenciando entre la situación actual y la situación objetivo:

#### 2.5.1 (actual)

> - **Autenticación de usuarios:** Uso de Firebase Auth para gestionar el acceso seguro mediante email/contraseña y proveedores sociales (Google, Apple, etc.).
> - **Reglas de seguridad en base de datos:** Configuración de reglas en Firebase Realtime Database para restringir el acceso y las operaciones según el usuario autenticado.
> - **Cifrado en tránsito:** Todo el tráfico entre cliente y servidor se realiza sobre HTTPS, garantizando la confidencialidad de los datos.
> - **Gestión de permisos:** Control de acceso a recursos (archivos, datos) mediante reglas de seguridad y roles definidos en Firebase.
> - **Notificaciones seguras:** Uso de Firebase Cloud Messaging con tokens de dispositivo para evitar envíos no autorizados.
> - **Actualizaciones automáticas:** El uso de Firebase Hosting y las tiendas de aplicaciones permite distribuir rápidamente parches de seguridad.

#### 2.5.2 (objetivo)

> - **Autenticación robusta:** Uso de Supabase Auth con soporte para OAuth, email y proveedores sociales, incluyendo autenticación multifactor (MFA) si es necesario.
> - **Row Level Security (RLS):** Implementación de políticas RLS en PostgreSQL para asegurar que cada usuario solo accede a sus propios datos, incluso ante accesos directos a la base de datos. [Referencia RLS](https://supabase.com/docs/guides/auth/row-level-security)
> - **Cifrado en tránsito y en reposo:** Todo el tráfico se realiza sobre HTTPS y los datos almacenados en Supabase están cifrados en reposo.
> - **Gestión avanzada de permisos:** Definición de roles y políticas de acceso granular en Supabase para recursos, archivos y funciones edge.
> - **Auditoría y trazabilidad:** Registro de eventos críticos y accesos a datos sensibles para facilitar la auditoría y el cumplimiento normativo.
> - **Protección contra ataques comunes:** Validación y sanitización de entradas, protección contra inyección SQL, XSS y CSRF en la PWA y microservicios Python.
> - **Actualizaciones y despliegue seguro:** Uso de CI/CD (GitHub Actions) para automatizar tests de seguridad y despliegues, minimizando errores humanos.
> - **Gestión segura de secretos:** Almacenamiento de claves y secretos en entornos seguros (variables de entorno, secretos de Supabase/GitHub Actions).
>
> Estas prácticas garantizan la protección de los datos de los usuarios y la integridad del sistema tanto en la situación actual como en la transición hacia la nueva arquitectura basada en Supabase y Python.

### **2.6. Tests**

#### 2.6.1 (actual)

> Actualmente, el proyecto cuenta con tests unitarios y de integración básicos, centrados en la lógica de negocio implementada en Angular y la interacción con Firebase. Se utilizan herramientas como Jasmine y Karma para tests unitarios, y Protractor para tests end-to-end. Los casos de uso principales cubiertos incluyen:
>
> - Alta, edición y borrado de alimentos en la despensa.
> - Sincronización de datos con Firebase.
> - Autenticación de usuarios y control de acceso.
> - Notificaciones de caducidad y agotamiento de productos.

#### 2.6.2 (objetivo)

> En la arquitectura objetivo, se amplía la cobertura de tests, incluyendo tests unitarios, de integración y end-to-end tanto para el frontend (PWA en Python) como para el backend (Supabase y microservicios Python). Se utilizarán herramientas como Pytest para Python, y frameworks de testing para PWA (por ejemplo, Playwright o Selenium para pruebas de interfaz).
>
> Se definen los siguientes casos de uso principales, detallados en formato Gherkin:
>
> **Caso de uso 1: Gestión de inventario de la despensa**
> ```gherkin
> Feature: Gestión de inventario
>   As a usuario
>   I want to añadir, editar y eliminar alimentos en mi despensa
>   So that pueda mantener un inventario actualizado
>
>   Scenario: Añadir un alimento
>     Given el usuario está autenticado
>     When añade un alimento con nombre "Manzana" y cantidad 5
>     Then el alimento aparece en la lista de la despensa
>
>   Scenario: Editar un alimento
>     Given existe un alimento "Manzana" en la despensa
>     When el usuario actualiza la cantidad a 10
>     Then la cantidad del alimento "Manzana" es 10
>
>   Scenario: Eliminar un alimento
>     Given existe un alimento "Manzana" en la despensa
>     When el usuario elimina el alimento
>     Then el alimento "Manzana" ya no aparece en la lista
> ```
>
> **Caso de uso 2: Planificación de menús saludables con IA**
> ```gherkin
> Feature: Sugerencia de menús saludables
>   As a usuario
>   I want to recibir sugerencias de menús personalizados según mis preferencias y mi inventario
>   So that pueda planificar mi alimentación de forma saludable
>
>   Scenario: Sugerencia de menú semanal
>     Given el usuario tiene alimentos disponibles en la despensa
>     When solicita una sugerencia de menú semanal
>     Then el sistema muestra un menú adaptado a sus preferencias y restricciones
> ```
>
> **Caso de uso 3: Sincronización y funcionalidad offline**
> ```gherkin
> Feature: Sincronización y modo offline
>   As a usuario
>   I want to poder usar la aplicación sin conexión y sincronizar los cambios al recuperar la conexión
>   So that no pierda información y pueda gestionar mi despensa en cualquier momento
>
>   Scenario: Añadir alimento sin conexión
>     Given el usuario está sin conexión
>     When añade un alimento a la despensa
>     Then el alimento se guarda localmente
>     And cuando se recupera la conexión, el alimento se sincroniza con el servidor
> ```
>
> **Caso de uso 4: Notificaciones inteligentes**
> ```gherkin
> Feature: Notificaciones de caducidad y compra
>   As a usuario
>   I want to recibir notificaciones cuando un alimento esté a punto de caducar o falte para una receta
>   So that pueda consumir los productos a tiempo y completar mis menús
>
>   Scenario: Notificación de caducidad próxima
>     Given un alimento caduca en 3 días
>     When se acerca la fecha de caducidad
>     Then el usuario recibe una notificación de aviso
> ```
>
> Estos tests aseguran la calidad, robustez y experiencia de usuario en la nueva arquitectura, cubriendo tanto la lógica de negocio como la integración con Supabase y el microservicio de IA.

---

## 3. Modelo de Datos

### **3.1. Diagrama del modelo de datos:**

#### **3.1.1 (actual)**

> ```mermaid
> erDiagram
>     USUARIOS ||--o{ ALIMENTOS : "tiene"
>     USUARIOS ||--o{ RECETAS : "tiene"
>     RECETAS ||--o{ INGREDIENTES : "contiene"
>     ALIMENTOS ||--o{ NOTIFICACIONES : "genera"
>
>     USUARIOS {
>         string id PK "Identificador único del usuario"
>         string nombre "Nombre del usuario"
>         string email "Correo electrónico del usuario"
>         string provider "Proveedor de autenticación (Google, Apple, etc.)"
>     }
>
>     ALIMENTOS {
>         string id PK "Identificador único del alimento"
>         string usuario_id FK "ID del usuario que posee el alimento"
>         string nombre "Nombre del alimento"
>         int cantidad "Cantidad del alimento"
>         string unidad "Unidad de medida (gramos, litros, etc.)"
>         date caducidad "Fecha de caducidad del alimento"
>     }
>
>     RECETAS {
>         string id PK "Identificador único de la receta"
>         string usuario_id FK "ID del usuario que posee la receta"
>         string nombre "Nombre de la receta"
>         string descripcion "Descripción de la receta"
>     }
>
>     INGREDIENTES {
>         string id PK "Identificador único del ingrediente"
>         string receta_id FK "ID de la receta a la que pertenece el ingrediente"
>         string alimento_id FK "ID del alimento que es el ingrediente"
>         int cantidad "Cantidad del ingrediente necesario"
>     }
>
>     NOTIFICACIONES {
>         string id PK "Identificador único de la notificación"
>         string alimento_id FK "ID del alimento que genera la notificación"
>         string mensaje "Mensaje de la notificación"
>         date fecha "Fecha de la notificación"
>     }
>

#### **3.1.2 (objetivo)**

> ```mermaid
> erDiagram
>     USUARIOS ||--o{ LISTAS : "crea"
>     LISTAS ||--o{ ALIMENTOS_LISTAS : "contiene"
>     ALIMENTOS ||--o{ ALIMENTOS_LISTAS : "pertenece a"
>     LISTAS ||--o{ LISTAS_USUARIOS : "compartida con"
>     USUARIOS ||--o{ LISTAS_USUARIOS : "acceso a"
>     USUARIOS ||--o{ ALIMENTOS : "tiene"
>     USUARIOS ||--o{ RECETAS : "tiene"
>     RECETAS ||--o{ INGREDIENTES : "contiene"
>     ALIMENTOS ||--o{ NOTIFICACIONES : "genera"
>     USUARIOS ||--o{ MENUS : "tiene"
>     MENUS ||--o{ RECETAS : "incluye"
>
>     USUARIOS {
>        uuid id PK "Identificador único del usuario"
>        string nombre "Nombre del usuario (NOT NULL)"
>        string email "Correo electrónico del usuario (NOT NULL, UNIQUE)"
>        jsonb metadata "Metadatos adicionales del usuario"
>     }
>
>     LISTAS {
>        uuid id PK "Identificador único de la lista"
>        string nombre "Nombre de la lista (NOT NULL)"
>        uuid propietario_id FK "ID del usuario propietario (NOT NULL)"
>        string tipo "Tipo de lista (personal, compra, compartida)"
>        string descripcion "Descripción de la lista"
>        timestamp fecha_creacion "Fecha de creación"
>     }
>
>     LISTAS_USUARIOS {
>        uuid lista_id FK "ID de la lista"
>        uuid usuario_id FK "ID del usuario con acceso"
>        string permisos "Permisos (lectura, edición, propietario)"
>     }
>
>     ALIMENTOS {
>        uuid id PK "Identificador único del alimento"
>        string nombre "Nombre del alimento (NOT NULL)"
>        int cantidad "Cantidad del alimento (NOT NULL)"
>        string unidad "Unidad de medida (gramos, litros, etc.) (NOT NULL)"
>        date caducidad "Fecha de caducidad del alimento (NOT NULL)"
>        uuid propietario_id FK "ID del usuario propietario (NOT NULL)"
>        jsonb metadata "Metadatos adicionales del alimento"
>     }
>
>     ALIMENTOS_LISTAS {
>        uuid alimento_id FK "ID del alimento"
>        uuid lista_id FK "ID de la lista"
>     }
>
>     RECETAS {
>        uuid id PK "Identificador único de la receta"
>        uuid propietario_id FK "ID del usuario que posee la receta (NOT NULL)"
>        string nombre "Nombre de la receta (NOT NULL)"
>        string descripcion "Descripción de la receta"
>        jsonb ingredientes "Lista de ingredientes en formato JSONB"
>     }
>
>     INGREDIENTES {
>        uuid id PK "Identificador único del ingrediente"
>        uuid receta_id FK "ID de la receta a la que pertenece el ingrediente (NOT NULL)"
>        uuid alimento_id FK "ID del alimento que es el ingrediente (NOT NULL)"
>        int cantidad "Cantidad del ingrediente necesario (NOT NULL)"
>     }
>
>     NOTIFICACIONES {
>        uuid id PK "Identificador único de la notificación"
>        uuid usuario_id FK "ID del usuario que recibe la notificación (NOT NULL)"
>        string mensaje "Mensaje de la notificación (NOT NULL)"
>        timestamp fecha "Fecha de la notificación (NOT NULL)"
>     }
>
>     MENUS {
>        uuid id PK "Identificador único del menú"
>        uuid usuario_id FK "ID del usuario que posee el menú (NOT NULL)"
>        date fecha_inicio "Fecha de inicio del menú (NOT NULL)"
>        date fecha_fin "Fecha de fin del menú (NOT NULL)"
>        jsonb recetas "Lista de recetas en formato JSONB"
>     }

### **3.2. Descripción de entidades principales:**

> - USUARIOS
>   - id (PK): Identificador único del usuario (UUID en el modelo objetivo).
>   - nombre: Nombre del usuario (NOT NULL en el modelo objetivo).
>   - email: Correo electrónico del usuario (NOT NULL y UNIQUE en el modelo objetivo).
>   - provider: Proveedor de autenticación (Google, Apple, etc.) (solo en el modelo actual).
>   - metadata: Metadatos adicionales del usuario en formato JSONB (solo en el modelo objetivo).
> - ALIMENTOS
>   - id (PK): Identificador único del alimento (UUID en el modelo objetivo).
>   - usuario_id (FK): ID del usuario que posee el alimento (NOT NULL en el modelo objetivo).
>   - nombre: Nombre del alimento (NOT NULL en el modelo objetivo).
>   - cantidad: Cantidad del alimento (NOT NULL en ambos modelos).
>   - unidad: Unidad de medida (gramos, litros, etc.) (NOT NULL en el modelo objetivo).
>   - caducidad: Fecha de caducidad del alimento (NOT NULL en el modelo objetivo).
>   - metadata: Metadatos adicionales del alimento en formato JSONB (solo en el modelo objetivo).
> - RECETAS
>   - id (PK): Identificador único de la receta (UUID en el modelo objetivo).
>   - usuario_id (FK): ID del usuario que posee la receta (NOT NULL en el modelo objetivo).
>   - nombre: Nombre de la receta (NOT NULL en el modelo objetivo).
>   - descripcion: Descripción de la receta.
>   - ingredientes: Lista de ingredientes en formato JSONB (solo en el modelo objetivo).
> - INGREDIENTES
>   - id (PK): Identificador único del ingrediente (UUID en el modelo objetivo).
>   - receta_id (FK): ID de la receta a la que pertenece el ingrediente (NOT NULL en el modelo objetivo).
>   - alimento_id (FK): ID del alimento que es el ingrediente (NOT NULL en el modelo objetivo).
>   - cantidad: Cantidad del ingrediente necesario (NOT NULL en ambos modelos).
> - NOTIFICACIONES
>   - id (PK): Identificador único de la notificación (UUID en el modelo objetivo).
>   - alimento_id (FK): ID del alimento que genera la notificación (NOT NULL en el modelo objetivo).
>   - mensaje: Mensaje de la notificación (NOT NULL en ambos modelos).
>   - fecha: Fecha de la notificación (NOT NULL en ambos modelos).
> - MENUS (solo en el modelo objetivo)
>   - id (PK): Identificador único del menú (UUID).
>   - usuario_id (FK): ID del usuario que posee el menú (NOT NULL).
>   - fecha_inicio: Fecha de inicio del menú (NOT NULL).
>   - fecha_fin: Fecha de fin del menú (NOT NULL).
>   - recetas: Lista de recetas en formato JSONB.
> - LISTAS
>   - id (PK): Identificador único de la lista (UUID).
>   - nombre: Nombre de la lista (NOT NULL).
>   - propietario_id (FK): ID del usuario propietario (NOT NULL).
>   - tipo: Tipo de lista (personal, compra, compartida).
>   - descripcion: Descripción de la lista.
>   - fecha_creacion: Fecha de creación.
> - LISTAS_USUARIOS
>   - lista_id (FK): ID de la lista.
>   - usuario_id (FK): ID del usuario con acceso.
>   - permisos: Permisos (lectura, edición, propietario).
> - ALIMENTOS_LISTAS
>   - alimento_id (FK): ID del alimento.
>   - lista_id (FK): ID de la lista.

> - Relaciones y Restricciones
>   - USUARIOS - ALIMENTOS: Un usuario puede tener muchos alimentos. Relación uno a muchos.
>   - USUARIOS - RECETAS: Un usuario puede tener muchas recetas. Relación uno a muchos.
>   - RECETAS - INGREDIENTES: Una receta puede tener muchos ingredientes. Relación uno a muchos.
>   - ALIMENTOS - NOTIFICACIONES: Un alimento puede generar muchas notificaciones. Relación uno a muchos.
>   - USUARIOS - MENUS: Un usuario puede tener muchos menús. Relación uno a muchos.
>   - MENUS - RECETAS: Un menú puede incluir muchas recetas. Relación uno a muchos.

> - Restricciones Adicionales
>   - NOT NULL: Campos obligatorios que no pueden ser nulos.
>   - UNIQUE: Campos que deben ser únicos en la tabla (por ejemplo, el email del usuario).
>   - PK: Clave primaria que identifica de manera única cada registro en la tabla.
>   - FK: Clave foránea que establece una relación con otra tabla.

---

## 4. Especificación de la API

Se define la especificación de la [API](openapi.yaml) objetivo del proyecto en formato OpenAPI.

Para facilitar el desarrollo y las pruebas, tanto para el frontend como para el backend, es recomendable utilizar herramientas que permitan visualizar y probar la API de manera sencilla, así como implementar mocks para simular el comportamiento de la API durante el desarrollo. A continuación, se detallan las recomendaciones:

### 1. **Visualización y Pruebas de la API**

#### **Herramienta Recomendada: Swagger UI**

Swagger UI es una herramienta ampliamente utilizada para visualizar y probar APIs definidas en formato OpenAPI. Permite a los desarrolladores interactuar con la API directamente desde el navegador, enviando solicitudes y viendo las respuestas en tiempo real.

**Pasos para implementar Swagger UI:**

1. **Generar la especificación OpenAPI**: Asegúrate de que la especificación OpenAPI esté completa y correctamente definida en un archivo `openapi.yaml` o `openapi.json`.

2. **Integrar Swagger UI en el proyecto**:
   - Si estás utilizando un framework como Flask o FastAPI en el backend, puedes integrar Swagger UI fácilmente con la librería `swagger-ui` o `fastapi` (que incluye Swagger UI por defecto).
   - Para otros frameworks, puedes servir el archivo OpenAPI y usar la interfaz de Swagger UI disponible en [Swagger UI](https://swagger.io/tools/swagger-ui/).

**Ejemplo de integración con FastAPI:**

```python
from fastapi import FastAPI
from fastapi.openapi.utils import get_openapi

app = FastAPI()

# Definir tus endpoints aquí

def custom_openapi():
    if app.openapi_schema:
        return app.openapi_schema
    openapi_schema = get_openapi(
        title="Alacena API",
        version="1.0.0",
        description="API para la gestión de la despensa, recetas, menús y notificaciones en la aplicación Alacena.",
        routes=app.routes,
    )
    app.openapi_schema = openapi_schema
    return app.openapi_schema

app.openapi = custom_openapi
```

3. **Acceder a Swagger UI**: Una vez que el servidor esté en funcionamiento, puedes acceder a la interfaz de Swagger UI en `http://localhost:8000/docs` (en el caso de FastAPI).

### 2. **Ejemplos de la API**

Es importante proporcionar ejemplos de solicitudes y respuestas para cada endpoint en la especificación OpenAPI. Esto ayuda a los desarrolladores a entender cómo interactuar con la API.

**Ejemplo de especificación OpenAPI con ejemplos:**

```yaml
paths:
  /usuarios:
    post:
      summary: Crear un nuevo usuario
      description: Crea un nuevo usuario en el sistema.
      requestBody:
        required: true
        content:
          application/json:
            schema:
              $ref: '#/components/schemas/Usuario'
            example:
              nombre: "Juan Pérez"
              email: "juan.perez@example.com"
      responses:
        '201':
          description: Usuario creado exitosamente
          content:
            application/json:
              schema:
                $ref: '#/components/schemas/Usuario'
              example:
                id: "550e8400-e29b-41d4-a716-446655440000"
                nombre: "Juan Pérez"
                email: "juan.perez@example.com"
```

### 3. **Mocks para Desarrollo y Pruebas**

#### **Herramienta Recomendada: JSON Server**

> JSON Server es una herramienta sencilla que permite crear un servidor RESTful a partir de un archivo JSON. Es ideal para simular el comportamiento de la API durante el desarrollo del frontend.
>
> **Pasos para implementar JSON Server:**
>
> 1. **Instalar JSON Server**:
>    ```bash
>    npm install -g json-server
>    ```
>
> 2. **Crear un archivo JSON con datos de ejemplo**:
>    ```json
>    {
>      "usuarios": [
>        {
>          "id": "550e8400-e29b-41d4-a716-446655440000",
>          "nombre": "Juan Pérez",
>          "email": "juan.perez@example.com"
>        }
>      ],
>      "alimentos": [
>        {
>          "id": "550e8400-e29b-41d4-a716-446655440001",
>          "usuario_id": "550e8400-e29b-41d4-a716-446655440000",
>          "nombre": "Manzana",
>          "cantidad": 5,
>          "unidad": "kg",
>          "caducidad": "2024-07-01"
>        }
>      ]
>    }
>    ```
>
> 3. **Iniciar JSON Server**:
>    ```bash
>    json-server --watch db.json
>    ```
>
> 4. **Interactuar con el servidor mock**: El servidor estará disponible en `http://localhost:3000`, y podrás realizar solicitudes GET, POST, PUT, DELETE, etc., como si fuera la API real.
>
> #### **Mocks en el Backend**
>
> Para el backend, puedes utilizar librerías como `unittest.mock` en Python para simular las respuestas de la API durante las pruebas unitarias.
>
> **Ejemplo de mock en Python:**
>
> ```python
> from unittest.mock import patch
> import requests
>
> def test_get_usuarios():
>     with patch('requests.get') as mock_get:
>         mock_get.return_value.status_code = 200
>         mock_get.return_value.json.return_value = [
>             {"id": "550e8400-e29b-41d4-a716-446655440000", "nombre": "Juan Pérez", "email": "juan.perez@example.com"}
>         ]
>
>         response = requests.get('http://localhost:3000/usuarios')
>         assert response.status_code == 200
>         assert response.json()[0]['nombre'] == "Juan Pérez"
> ```
>
> ### Resumen
>
> - **Swagger UI**: Para visualizar y probar la API de manera interactiva.
> - **Ejemplos en OpenAPI**: Para proporcionar ejemplos claros de solicitudes y respuestas.
> - **JSON Server**: Para crear un servidor mock que simule la API durante el desarrollo del frontend.
> - **unittest.mock**: Para simular respuestas de la API en pruebas unitarias del backend.
>
> Estas herramientas y prácticas facilitarán el desarrollo, las pruebas y la colaboración entre los equipos de frontend y backend.

---

## 5. Historias de Usuario

> Se ha definido la documentación más completa posible, en base a todo lo establecido en este documento y los ficheros creados al definir este documento, y se han creado los documentos necesarios para crear las historias de usuario de la siguiente manera:

> - [Documento prd](analisis/prd.md)
> - [Diagrama C4](analisis/DiagramaC4.md)
> - [Planificación a largo plazo](analisis/PlanificacionLargoPlazo.md)
> - [Planificación de Releases y roadmap](analisis/PlanificacionReleasesRoadmap.md)
> - [Checklist sobre el analisis realizado](analisis/ChecklistAnalisis.md)
> - [Backlog priorizado](analisis/backlog/BacklogPriorizado.md)
> - [Épicas de trabajo](analisis/backlog/Epicas.md)
> - Historias de usuario:
>   - [HU_1](analisis/backlog/HU_1.md)
>   - [HU_2](analisis/backlog/HU_2.md)
>   - [HU_3](analisis/backlog/HU_3.md)
>   - [HU_4](analisis/backlog/HU_4.md)
>   - [HU_5](analisis/backlog/HU_5.md)
>   - [HU_6](analisis/backlog/HU_6.md)
>   - [HU_7](analisis/backlog/HU_7.md)
>   - [HU_8](analisis/backlog/HU_8.md)
>   - [HU_9](analisis/backlog/HU_9.md)
>   - [HU_10](analisis/backlog/HU_10.md)
>   - [HU_11](analisis/backlog/HU_11.md)

---

## 6. Commits y Releases
**Commit [d11bce6](https://github.com/DanielContrerasAladro/Alacena/commit/d11bce6):**
- **Descripción:** chore: revisión de readme y changelog precommit
- **Cambios:** [Descripción de los cambios]
- **Release:** No genera release

> Al seguir un enfoque [Trunk-Based Development](https://trunkbaseddevelopment.com/), cada vez que se complete una historia de usuario o un ticket de trabajo, se generará un commit en lugar de PR, que seguirán la convención de commit de [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/), y se documentará en el fichero de log de cambios @CHANGELOG.md, que se generará automáticamente al hacer un commit. El formato del commit será el siguiente:
>
> ```
> docs: [descripción breve]
> chore: [descripción breve] <para tareas de arquitectura, refactorización, etc.>
> feat: [historia de usuario o ticket de trabajo] - [descripción breve]
> fix: [historia de usuario o ticket de trabajo] - [descripción breve] <bugs encontrados y corregidos tras la revisión de los feat>
> ````

>**Commit [d69021c](https://github.com/DanielContrerasAladro/AI4Devs-finalproject/commit/d69021c):**
>  - **Descripción:** docs: documentacion de arquitectura de proyecto, punto de partida y propuesta de refactorizacion
>  - **Cambios:** Documentación de arquitectura del proyecto, punto de partida y propuesta de refactorización.
>  - **Release:** No genera release

>**Commit [f47e3c6](https://github.com/DanielContrerasAladro/AI4Devs-finalproject/commit/f47e3c6):**
>  - **Descripción:** docs: documentacion de arquitectura de proyecto, punto de partida y propuesta de refactorizacion
>  - **Cambios:** Documentación de arquitectura del proyecto, punto de partida y propuesta de refactorización.
>  - **Release:** No genera release

>**Commit [e321125](https://github.com/DanielContrerasAladro/AI4Devs-finalproject/commit/e321125):**
>  - **Descripción:** docs: ajuste formato diagramas
>  - **Cambios:** Ajuste en el formato de los diagramas.
>  - **Release:** No genera release

>**Commit [5ca2e6e](https://github.com/DanielContrerasAladro/AI4Devs-finalproject/commit/5ca2e6e):**
>  - **Descripción:** docs: diagrama de entidad relación y descripción de entidades
>  - **Cambios:** Diagrama de entidad relación y descripción de entidades.
>  - **Release:** No genera release

>**Commit [edfedc9](https://github.com/DanielContrerasAladro/AI4Devs-finalproject/commit/edfedc9):**
>  - **Descripción:** docs: documentos de análisis, planificación y primera definición de historias de usuario
>  - **Cambios:** Documentos de análisis, planificación y primera definición de historias de usuario.
>  - **Release:** No genera release

>**Commit [76bef8d](https://github.com/DanielContrerasAladro/AI4Devs-finalproject/commit/76bef8d):**
>  - **Descripción:** chore: ajuste URL del repositorio del proyecto
>  - **Cambios:** Ajuste en la URL del repositorio del proyecto.
>  - **Release:** No genera release

> **Commit [](https://github.com/DanielContrerasAladro/AI4Devs-finalproject/commit/d14b283):**
>  - **Descripción:**
>  - **Cambios:** [Descripción de los cambios]
>  - **Release:** No genera release

> **Commit [d11bce6](https://github.com/DanielContrerasAladro/Alacena/commit/d11bce6):**
> - **Descripción:** chore: revisión de readme y changelog precommit
> - **Cambios:** [Descripción de los cambios]
> - **Release:** No genera release


> **Commit [f65d9fa](https://github.com/DanielContrerasAladro/Alacena/commit/f65d9fa):**
> - **Descripción:** Update deploy.yml
> - **Cambios:** [Descripción de los cambios]
> - **Release:** No genera release


> **Commit [cae233d](https://github.com/DanielContrerasAladro/Alacena/commit/cae233d):**
> - **Descripción:** feat(hu1_hu2_hu5): reestructuracion codigo, tests unitarios, y login completo
> - **Cambios:** [Descripción de los cambios]
> - **Release:** No genera release


> **Commit [cae233d](https://github.com/DanielContrerasAladro/Alacena/commit/cae233d):**
> - **Descripción:** feat(hu1_hu2_hu5): reestructuracion codigo, tests unitarios, y login completo
> - **Cambios:** [Descripción de los cambios]
> - **Release:** No genera release


> **Commit [cae233d](https://github.com/DanielContrerasAladro/Alacena/commit/cae233d):**
> - **Descripción:** feat(hu1_hu2_hu5): reestructuracion codigo, tests unitarios, y login completo
> - **Cambios:** [Descripción de los cambios]
> - **Release:** No genera release


> **Commit [cae233d](https://github.com/DanielContrerasAladro/Alacena/commit/cae233d):**
> - **Descripción:** feat(hu1_hu2_hu5): reestructuracion codigo, tests unitarios, y login completo
> - **Cambios:** [Descripción de los cambios]
> - **Release:** No genera release


> **Commit [7ee9135](https://github.com/DanielContrerasAladro/Alacena/commit/7ee9135):**
> - **Descripción:** docs: documentos de análisis, planificación y primera definición de historias de usuario redefinidos tras primer sprint
> - **Cambios:** [Descripción de los cambios]
> - **Release:** No genera release


> **Commit [feadad6](https://github.com/DanielContrerasAladro/Alacena/commit/feadad6):**
> - **Descripción:** chore: readme y changelog precommi corregido
> - **Cambios:** [Descripción de los cambios]
> - **Release:** No genera release


> **Commit [4687841](https://github.com/DanielContrerasAladro/Alacena/commit/4687841):**
> - **Descripción:** chore: readme con uso de precommit
> - **Cambios:** [Descripción de los cambios]
> - **Release:** No genera release


> **Commit [4687841](https://github.com/DanielContrerasAladro/Alacena/commit/4687841):**
> - **Descripción:** chore: readme con uso de precommit
> - **Cambios:** [Descripción de los cambios]
> - **Release:** No genera release

