> Detalla en esta sección los prompts principales utilizados durante la creación del proyecto, que justifiquen el uso de asistentes de código en todas las fases del ciclo de vida del desarrollo. Esperamos un máximo de 3 por sección, principalmente los de creación inicial o  los de corrección o adición de funcionalidades que consideres más relevantes.
Puedes añadir adicionalmente la conversación completa como link o archivo adjunto si así lo consideras


## Índice

- [Índice](#índice)
- [1. Descripción general del producto](#1-descripción-general-del-producto)
- [2. Arquitectura del Sistema](#2-arquitectura-del-sistema)
  - [**2.1. Diagrama de arquitectura:**](#21-diagrama-de-arquitectura)
  - [**2.2. Descripción de componentes principales:**](#22-descripción-de-componentes-principales)
  - [**2.3. Descripción de alto nivel del proyecto y estructura de ficheros**](#23-descripción-de-alto-nivel-del-proyecto-y-estructura-de-ficheros)
  - [**2.4. Infraestructura y despliegue**](#24-infraestructura-y-despliegue)
  - [**2.5. Seguridad**](#25-seguridad)
  - [**2.6. Tests**](#26-tests)
- [3. Modelo de Datos](#3-modelo-de-datos)
- [4. Especificación de la API](#4-especificación-de-la-api)
- [5. Historias de Usuario y Tickets de Trabajo](#5-historias-de-usuario-y-tickets-de-trabajo)
- [6. Desarrollo de las Historias de Usuario del proyecto](#6-desarrollo-de-las-historias-de-usuario-del-proyecto)
  - [6.1 Preparación repositorio](#61-preparación-repositorio)
  - [6.2 Commits y releases](#62-commits-y-releases)

---

## 1. Descripción general del producto

**Prompt 1:**

Como experto desarrollador de aplicaciones para móviles, revisa el código del proyecto @Codebase  y crea un solution spec en formato markdown en la carpeta @refactor  siguiendo los estándares para este tipo de documentos, ten en cuenta que este documento será el punto de partida para el personal de negocio, de desarrollo, de infrastructura y de diseño para realizar una refactorización del código fuente de la aplicación

**Prompt 2:**

Perfecto, ahora revisa el @Codebase y rellena el documento con la información que puedas extraer del código fuente y los fiocheros de configuración del mismo

**Prompt 3:**

ahora actúa como desarrollador expero en applicaciones móviles y continúa documentando el proyecto en el @solution_spec.md

**Prompt 4:**

Actúa como un experto en producto de negocio rellenar los apartados 0 y 1 en @readme.md en base a lo indicado en @readme.md , teniendo en cuenta la documentación anterior @solution_spec.md y que el alcance del proyecto debe tener 30 horas de duración para obtener un MVP, si tienes dudas sobre algún punto  sobre el que rellenar pregúntame

**Prompt 5:**

Lee el listado de @alcance.md y modifica el apartado 1 de @readme.md para que el objetivo, características y diseño reflejen lo especificado como características del proyecto

**Prompt 6:**

Como experto arquitecto de software, necesito que crees un diagrama mermaid que represente el funcionamiento del proyecto a día de hoy según @solution_spec.md

**Prompt 7:**

Como arquitecto de software experto en refactorización, con conocimientos en @Doc_AngularJS @Doc_Angular @Ionic Framework @Firebase @Sign in with Apple @Google Sign-In @Reflex @Django PWA @Django @Flask @Python 3 Javascript y Typescript, revisa el código del proyecto, el fichero @solution_spec.md y el apartado '2.1. Diagrama de arquitectura:(actual)' y previos del documento @readme.md para realizar una propuesta de refactorización, en un documento markdown en la carpeta @refactor, del código del proyecto teniendo en cuenta lo descrito en @alcance.md, el objetivo princiopal es reescribir el proyecto para traerlo a la úlñtima versiñón de un framework y convertirlo de app para dispositivos a PWA responsive

**Prompt 8:**

antes de continuar, revisando la propuesta con el equipo de desarrollo, expertos en python con algunos conocimientos de Angular e ionic, y teniendo en cuenta la idea de añadir un agente de IA en el proyecto, arguménta porqué no reescribirlo todo en Python

**Prompt 9:**

antes de continuar, revisando la propuesta con el equipo de desarrollo, expertos en python con algunos conocimientos de Angular e ionic, y teniendo en cuenta la idea de añadir un agente de IA en el proyecto, arguménta porqué no reescribirlo todo en Python

**Prompt 10:**

Si, realiza una comparativa de costes para incluirla en el documento de propuesta, pero el equipo de desarrollo ha evaluado Supabase por su lado y prefiere que esta sea la opción para la arquitectura, adapta la propuesta de refactorización enfocándote en esta opción y teniendo en cuenta esto que han encontrado los desarrolladores  @Supabase Python y la documentación de @Supabase

**Prompt 11:**

Amplía la propuesta con ejemplos de uso de supabase-py y @https://medium.com/@rohitverma_69543/harnessing-the-power-of-supabase-in-python-with-supabase-py-03f36a97c482  el frontend debería también ser reescrito con Python, y con la información relevante de estas páginas, pues lo que proponen será tenido en cuenta en el proyecto, si tienes que adaptar la propuesta hazlo @https://supabase.com/blog/sql-or-nosql-both-with-postgresql @https://supabase.com/docs/guides/getting-started/ai-prompts

**Prompt 12:**

Actualiza el proyecto de propuesta y crea también un fichero de log, en formato markdown con fecha y hora, que registre toda esta conversación y un documento markdown de resumen para saber cómo hemos llegado a la propuesta definitiva

---

## 2. Arquitectura del Sistema

### **2.1. Diagrama de arquitectura:**

**Prompt 1:**

Como experto arquitecto de software, necesito que crees un diagrama mermaid que represente el funcionamiento del proyecto a día de hoy según @solution_spec.md

**Prompt 2:**

@readme.md añade un apartado '### Explicación' en el apartado '### **2.1.2 (objetivo)**' que explique el diagrama igual que en el apartado '### **2.1.1 (actual)**'

### **2.2. Descripción de componentes principales:**

**Prompt 1:**

En base a @propuesta_refactorizacion.md, @solution_spec.md  y lo escrito ya en el fichero @readme.md incluye una descrpción técnica muy resumida de los componentes principales del proyecto, en el apartado '### **2.2. Descripción de componentes principales:**', cada componente debe definir la tecnología utilizada actualmente en el proyecto y la tecnología objetivo que debe utilizar, si puedes incluye algún ejemplo o referencia

### **2.3. Descripción de alto nivel del proyecto y estructura de ficheros**

**Prompt 1:**

En base a @propuesta_refactorizacion.md, @solution_spec.md  y lo escrito ya en el fichero @readme.md incluye una descrpción técnica muy resumida del proyecto, en el apartado '### **2.3. Descripción de alto nivel del proyecto y estructura de ficheros**', unas 4 o 5 líneas, y un diagrasma mermaid de la estructura de ficheros. Debes escribir dos apartados, uno con al situación actual y otro con la situación objetivo, como se ha hecho en '### **2.1. Diagrama de arquitectura:**'

### **2.4. Infraestructura y despliegue**

**Prompt 1:**

En base a @propuesta_refactorizacion.md, @solution_spec.md  y lo escrito ya en el fichero @readme.md incluye una descrpción técnica de la infrastructura del proyecto, en el apartado '### **2.4. Infraestructura y despliegue**', debes definir y crear un diagrama de infraestructura en formato mermaid válido la infraestructura utilizada actualmente en el proyecto y la infraestructura objetivo que debe utilizar, incluye también una explicación de cómo realizar despliegues en cada uno de los casos

### **2.5. Seguridad**

**Prompt 1:**

En base a @propuesta_refactorizacion.md, @solution_spec.md  y lo escrito ya en el fichero @readme.md, habla con los expertos en seguridad e incluye los requisitos y elementos de seguridad proyecto, en el apartado '### **2.5. Seguridad**', incluye y enumera las prácticas de seguridad principales implementadas actualmente en el proyecto y objetivo que se deban implementar

### **2.6. Tests**

**Prompt 1:**

En base a @propuesta_refactorizacion.md, @solution_spec.md  y lo escrito ya en el fichero @readme.md, habla con QA e incluye lostests definidos en el proyecto, en el apartado '### **2.6. Tests**', haz una breve descripción de los casos de uso actuales del proyecto, y detalla más en profundidad los tests y los casos de uso con formato gherkin para el objetivo del proyecto

---

## 3. Modelo de Datos

**Prompt 1:**

Actúa como experto en bases de datos @Postgres y con conocimientos en @Firebase @Ionic Framework @Supabase Python revisa el proyecto en base a @propuesta_refactorizacion.md, @solution_spec.md  y lo escrito ya en el fichero @readme.md, genera un diagrama en formato mermaid con el modelo de datos actual del proyecto y con un modelo de datos en base al objetivo del proyecto

**Prompt 2:**

Perfecto, amplía los dos diagramas en formato mermaid y añade todos los parámetros que permite la sintaxis para dar el máximo detalle, por ejemplo las claves primarias y foráneas. También revisa el formato markdown del documento @readme.md y dame una descripción con el máximo detalle de cada entidad, como el nombre y tipo de cada atributo, descripción breve si procede, claves primarias y foráneas, relaciones y tipo de relación, restricciones (unique, not null…), etc.

---

## 4. Especificación de la API

**Prompt 1:**

Actúa como experto en desarrollo backend de APIs con @Supabase @Supabase Python @Python 3 revisa el proyecto en base a @propuesta_refactorizacion.md, @solution_spec.md  y lo escrito ya en el fichero @readme.md, de ser necesaria una API en el objetivo del proyecto, describe los endpoints principales de la API  en formato OpenAPI con el mayor nivel de detalle posible. Sigue las buenas prácticas estándar de diseño de APIS, usa la metodología DDD y sigue los principios SOLID y DRY

**Prompt 2:**

Perfecto, los desarrolladores, tanto frontend como backend, piden que se especifiquen ejemplos de la API, así como una manera más sencilla y visual para verla, recomienda la mejor manera, y habrá que especificar, para el desarrollo y las pruebas, una forma de trabajar con mocks tanto para frontend como para backend

---

## 5. Historias de Usuario y Tickets de Trabajo

**Prompt 1:**

Actúa como experto analista de negocio que está teniendo conversaciones con el cliente y el product owner revisando los documentos @alcance.md@solution_spec.md  @propuesta_refactorizacion.md @readme.md para:
- definir un PRD en un documento markdown en la carpeta @analisis
- definir un Diagrama C4 que llegue en profundidad a los componentes del sistema, un documento markdown en la carpeta @analisis
- definir una planificación a largo plazo en base a los documentos creados y existentes, un documento markdown en la carpeta @analisis
- definir las Historias de Usuario, agrupándolas en Épicas funcionales, guárdalas en una carpeta que se llame backlog (créala si no ecxiste dentro de la carpeta @analisis, cada una en un documento markdown, con el formato siguiente:
```
Título de la Historia de Usuario:

Como [rol del usuario],
quiero [acción que desea realizar el usuario],
para que [beneficio que espera obtener el usuario].

Criterios de Aceptación:
[Detalle específico de funcionalidad]

Notas Adicionales:
[Cualquier consideración adicional]

Historias de Usuario Relacionadas:
[Relaciones con otras historias de usuario]
```
- definir el backlog para el proyecto, priorizando las historias de usuario generadas en base a MoSCoW
- define, para cada historia de usuario, los tickets de trabajo o subtareas sobre la historia de usuario, aterrízalos a nivel técnico, los perfiles técnicos particiopantes necesarios aportan su visión en este apartado, incluso agrúpalos para los diferentes pefiles técnicos, siendo la salida de una reunión de planificación y refinamiento
- Para cada ticket de trabajo debes dar una estimación según la metodología de tallas de camiseta, aquí deberías tomar el rol de los diferentes perfiles técnicos en que hayas agrupado los tickets de trabajo. agrúpa toda la información en un fichero markdwon por cada historia de usuario enriquecido con diagramas mermaid si es necesario, en la misma carpeta que esté el backlog

**Prompt 2:**

---

## 6. Desarrollo de las Historias de Usuario del proyecto

> Cada prompt será enlazado con el commit o release correspondiente, que se documentará para seguimiento del avance del proyecto tanto el el fichero [readme.md](readme.md) como en el [CHANGELOG.md](CHANGELOG.md) del proyecto.
> Ejemplo de log de commit:
> **Commit [N](https://github.com/DanielContrerasAladro/AI4Devs-finalproject/commit/1234567890abcdef1234567890abcdef12345678):**
>   - **Descripción:**
>   - **Cambios:**
>   - **Release:** [0.0.1](https://github.com/DanielContrerasAladro/AI4Devs-finalproject/releases/tag/0.0.1) o No genera release

---

### 6.1 Preparación repositorio

> **Prompt 1:**
> Como experto en @https://www.conventionalcommits.org/en/v1.0.0/#summary @GitHub Actions y commits en github, prepara el proyecto para que rellene el fichero @CHANGELOG.md al hacer un commit con el formato que tiene ahora mismo con el nuevo commit al principio del fichero, así como el fichero @readme.md con el commit en el mismo formato y en el apartado '## 6. Commits y Releases', a continuación del último commit, al final del fichero

> **Prompt 2:**
>

### 6.2 Commits y releases

> **Prompt Commit [N]:**
>
