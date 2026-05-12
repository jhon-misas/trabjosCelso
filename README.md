Red Social Simplificada - Sistema de Gestión de Amistades y Publicaciones
Integrantes:

Jhon Misas - 2220242047

David Mahecha - 222024


Descripción del Proyecto
Este programa implementa una red social simplificada que permite gestionar usuarios, publicaciones y amistades. El sistema facilita la interacción entre usuarios mediante una interfaz gráfica intuitiva.

Funcionalidades principales:

Crear nuevos usuarios

Buscar usuarios por username

Ver perfil de usuario (nombre, username, publicaciones, amigos)

Publicar mensajes con fecha automática

Agregar y ver amigos (usando estructura de grafo)

Eliminar usuario(Elimina sus publicaciones y las amistades)

Visualización de publicaciones en tarjetas


Estructura del proyecto:

RedSocialSimplificada/
├── interfaz/
│   ├── RedSocialSimplificada.java    (Ventana principal)
│   ├── PanelBusqueda.java             (Búsqueda y botones)
│   ├── PanelPerfil.java               (Perfil del usuario)
│   └── PanelPublicaciones.java        (Lista de publicaciones)
└── mundo/
    ├── Usuario.java                   (Entidad usuario)
    ├── Publicacion.java               (Entidad publicación)
    └── GrafoAmistades.java            (Estructura de amistades)



UML
┌─────────────────────┐     ┌─────────────────────┐
│ RedSocialSimplificada│     │    PanelBusqueda    │
├─────────────────────┤     ├─────────────────────┤
│ -panelBusqueda      │────▶│ -txtBuscar          │
│ -panelPerfil        │     │ -ventana            │
│ -panelPublicaciones │     └─────────────────────┘
│ -usuarios           │
│ -grafo              │     ┌─────────────────────┐
└──────────┬──────────┘     │    PanelPerfil      │
           │                ├─────────────────────┤
           ▼                │ -lblNombre          │
┌─────────────────────┐     │ -lblInfo            │
│   GrafoAmistades    │     │ -usuarioActual      │
├─────────────────────┤     └─────────────────────┘
│ -grafo: HashMap     │
└─────────────────────┘     ┌─────────────────────┐
           │                │ PanelPublicaciones  │
           ▼                ├─────────────────────┤
┌─────────────────────┐     │ -panelContenido     │
│      Usuario        │     │ -ventana            │
├─────────────────────┤     └─────────────────────┘
│ -username           │
│ -nombre             │     ┌─────────────────────┐
│ -publicaciones      │────▶│    Publicacion      │
│ -amigos             │     ├─────────────────────┤
└─────────────────────┘     │ -descripcion        │
                            │ -timeline           │
                            └─────────────────────┘



Conclusiones

Se logró implementar una red social funcional con operaciones CRUD básicas

El uso del grafo permite gestionar eficientemente las relaciones de amistad

La interfaz gráfica en Swing proporciona una experiencia de usuario intuitiva

El sistema es extensible para agregar más funcionalidades (likes, comentarios)






