# Diagrama C4 del Sistema

## 1. Diagrama de Contexto

```mermaid
C4Context
    Person(user, "Usuario", "Gestiona su alacena, menús y listas de la compra")
    Person(admin, "Administrador", "Administra usuarios y configuración global")
    System_Boundary(s1, "Alacena PWA") {
        System(alacena, "Alacena", "Aplicación web progresiva para gestión de despensa, menús y compras")
    }
    System_Ext(ia, "Servicio IA Nutricional", "Provee recomendaciones inteligentes de menús y compras")
    System_Ext(email, "Proveedor de Email", "Envía notificaciones y recuperación de contraseña")
    System_Ext(iot, "Dispositivos IoT", "Sensores y balanzas conectadas a la alacena")

    user -> alacena : Usa desde navegador
    admin -> alacena : Administra
    alacena -> ia : Solicita recomendaciones
    alacena -> email : Envía notificaciones
    alacena -> iot : Recibe datos automáticos
```

## 2. Diagrama de Contenedores

```mermaid
C4Container
    System_Boundary(s1, "Alacena PWA") {
        Container(web, "Frontend PWA", "Python (PyScript/Anvil)", "Interfaz de usuario multiplataforma")
        Container(api, "API Backend", "FastAPI (Python)", "Lógica de negocio, autenticación y gestión de datos")
        Container(db, "Base de Datos", "PostgreSQL", "Persistencia de usuarios, productos, movimientos, menús, listas")
        Container(swagger, "Swagger UI", "OpenAPI/Swagger", "Documentación interactiva de la API")
        Container(mock, "JSON Server", "Node.js", "Mock API para desarrollo frontend")
        Container(ia, "Módulo IA", "Python", "Recomendaciones inteligentes de menús y compras")
    }

    user -> web : Interacción UI
    admin -> web : Administración
    web -> api : Solicita datos y operaciones (REST)
    api -> db : CRUD entidades
    api -> swagger : Expone documentación
    web -> mock : Usa API simulada (desarrollo)
    api -> ia : Solicita recomendaciones
    api -> email : Envía notificaciones
    api -> iot : Recibe datos automáticos
```

## 3. Diagrama de Componentes

```mermaid
C4Component
    Container_Boundary(api, "API Backend (FastAPI)") {
        Component(auth, "Autenticación y Autorización", "JWT, OAuth2", "Login, registro, recuperación de contraseña, roles")
        Component(users, "Gestión de Usuarios", "FastAPI", "CRUD de usuarios y preferencias")
        Component(pantry, "Gestión de Alacena", "FastAPI", "CRUD de productos, movimientos e inventario")
        Component(menus, "Gestión de Menús y Recomendaciones", "FastAPI + IA", "Planificación de menús, integración IA")
        Component(shopping, "Gestión de Listas de la Compra", "FastAPI", "Generación y gestión de listas de la compra")
        Component(notifications, "Notificaciones", "FastAPI", "Gestión y envío de notificaciones")
        Component(iot, "Integración IoT", "FastAPI", "Recepción y procesamiento de datos de dispositivos")
        Component(openapi, "Documentación OpenAPI", "FastAPI/OpenAPI", "Generación de documentación Swagger")
    }

    web -> auth : Login/Logout/Registro
    web -> users : Perfil y preferencias
    web -> pantry : Productos y movimientos
    web -> menus : Menús y recomendaciones
    web -> shopping : Listas de la compra
    web -> notifications : Configuración de notificaciones
    iot -> pantry : Actualización automática de inventario
    api -> openapi : Documentación interactiva
    api -> db : Persistencia
```

## 4. Diagrama de Clases (Modelo de Datos Real)

```mermaid
classDiagram
    class Usuario {
        +id: UUID
        +nombre: str
        +email: str
        +password: str
        +fecha_registro: datetime
        +preferencias: PreferenciasUsuario
        --
        <<PK>> id
        <<Unique>> email
        <<Index>> fecha_registro
        <<Validation>> email formato válido, password hash, nombre requerido
    }
    class PreferenciasUsuario {
        +id: UUID
        +usuario_id: UUID
        +notificaciones: bool
        +restricciones_alimentarias: str
        +idioma: str
        --
        <<PK>> id
        <<FK>> usuario_id -> Usuario.id
    }
    class Producto {
        +id: UUID
        +nombre: str
        +categoria: str
        +cantidad: int
        +unidad: str
        +fecha_caducidad: date
        +usuario_id: UUID
        --
        <<PK>> id
        <<FK>> usuario_id -> Usuario.id
        <<Index>> fecha_caducidad
        <<Validation>> nombre requerido, cantidad >= 0, fecha_caducidad opcional
    }
    class Movimiento {
        +id: UUID
        +producto_id: UUID
        +usuario_id: UUID
        +tipo: MovimientoTipo
        +cantidad: int
        +fecha: datetime
        +descripcion: str
        --
        <<PK>> id
        <<FK>> producto_id -> Producto.id
        <<FK>> usuario_id -> Usuario.id
        <<Index>> fecha
        <<Validation>> cantidad != 0, tipo in {entrada, salida, ajuste}
    }
    class ListaCompra {
        +id: UUID
        +usuario_id: UUID
        +fecha_creacion: datetime
        +nombre: str
        +estado: ListaEstado
        --
        <<PK>> id
        <<FK>> usuario_id -> Usuario.id
        <<Index>> fecha_creacion
        <<Validation>> nombre requerido, estado in {pendiente, completada, cancelada}
    }
    class ItemListaCompra {
        +id: UUID
        +lista_id: UUID
        +producto_id: UUID
        +cantidad: int
        +comprado: bool
        --
        <<PK>> id
        <<FK>> lista_id -> ListaCompra.id
        <<FK>> producto_id -> Producto.id
        <<Validation>> cantidad > 0
    }
    class MenuSugerido {
        +id: UUID
        +usuario_id: UUID
        +fecha: date
        +descripcion: str
        +aceptado: bool
        --
        <<PK>> id
        <<FK>> usuario_id -> Usuario.id
        <<Index>> fecha
        <<Validation>> descripcion requerido
    }
    Usuario "1" -- "N" Producto : posee
    Usuario "1" -- "N" Movimiento : realiza
    Producto "1" -- "N" Movimiento : está relacionado
    Usuario "1" -- "N" ListaCompra : crea
    ListaCompra "1" -- "N" ItemListaCompra : contiene
    Producto "1" -- "N" ItemListaCompra : incluido_en
    Usuario "1" -- "N" MenuSugerido : recibe
    Usuario "1" -- "1" PreferenciasUsuario : tiene
```
