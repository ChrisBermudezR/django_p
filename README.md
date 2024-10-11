 # Requerimientos 

    - Python
    - Programación Orientada a Objetos
    - HTML
    - CSS

# Entornos  Virtuales

Son necesarios para no entrar en conflicto con las diferentes versiones de python.

Comando para crear entornos virtuales:

```python

#Instalr creador de ambientes virtuales
pip install virtualenv

#Crea entornos virtuales
virtualenv d:/CURSOS/Django_platzi/.envs/my-first-env 

#lista los entornos
ls d:/CURSOS/Django_platzi/.envs/

#Activa entornos virtuales
.envs\my-first-env\Scripts\activate
``` 


# Instalación de DJANGO

```python
pip install  django
```

Comandos:

```python

django-admin
```

Crear un proyecto:

```python

django-admin startproject nombre_proyecto # asi crea una carpeta con una carpeta duplicada dentro
django-admin startproject nombre_proyecto . #el punto hace que se cree el proyecto a la altura de la raíz y que no duplique la carpeta
```

# Correr el proyecto

```python
python manage.py runserver
```

# Model, View & Template

En Django, el concepto Model-View-Template (MVT) es una variante del patrón de arquitectura Model-View-Controller (MVC). En MVT, los componentes principales son:

- Model (Modelo):
        Representa los datos y la lógica de negocio de la aplicación. Los modelos en Django están vinculados a bases de datos, lo que permite definir las estructuras de datos y gestionar las consultas de forma eficiente. Cada clase de modelo generalmente corresponde a una tabla en la base de datos.

Ejemplo: Definir una clase Usuario que guarda información como nombre, correo, etc.

- View (Vista):
        Maneja la lógica de presentación. Las vistas en Django reciben las peticiones del usuario, interactúan con los modelos para obtener o manipular datos y devuelven una respuesta, generalmente en forma de página HTML. La vista es responsable de seleccionar qué datos mostrar y cómo procesar la solicitud del usuario.

Ejemplo: Una vista puede mostrar una lista de usuarios, o manejar la lógica de envío de formularios.

- Template (Plantilla):
        Es la capa de presentación o interfaz con el usuario. Los templates en Django son archivos HTML que pueden incluir etiquetas y variables de Django para renderizar dinámicamente contenido basado en los datos del modelo. Los templates permiten separar la lógica de negocio de la presentación, facilitando el desarrollo.

Ejemplo: Una plantilla HTML puede mostrar un formulario o la información de un perfil de usuario.

El flujo típico en Django es:

    El usuario hace una solicitud (request).
    Una vista recibe la solicitud y puede usar un modelo para obtener o modificar datos.
    La vista pasa los datos obtenidos a un template que genera el HTML para devolver al navegador del usuario como respuesta.

Este enfoque facilita la separación de responsabilidades y mejora el mantenimiento del código.


# Creación de una app

```python
python manage.py startapp my_first_app
```

# ORM (Object-Relational Mapping)

Un ORM (Object-Relational Mapping) es una técnica de programación que permite interactuar con bases de datos relacionales usando un modelo orientado a objetos. En lugar de escribir consultas SQL directamente, los desarrolladores pueden trabajar con las bases de datos mediante el uso de objetos y sus métodos, lo que simplifica la integración de bases de datos en aplicaciones.

Con un ORM, las tablas de la base de datos se mapean a clases de programación, las filas de las tablas a instancias de esas clases, y las columnas de las tablas a atributos de las clases. Esto permite realizar operaciones como crear, leer, actualizar y eliminar registros en la base de datos utilizando código en lugar de SQL.

Por ejemplo, en Python, los ORM como *SQLAlchemy* o Django *ORM* permiten manipular bases de datos de manera más sencilla. Aquí un ejemplo básico con *SQLAlchemy*:


Los ORMs son tecnologías que nos permiten gestionar nuestra base de datos, en todo el sentido de la palabra. No importa que tipo de motor de base de datos tenemos. Por medio del ORM, todo lo gestionamos igual, como por ejemplo:

    La estructura de nuestra base de datos, creación de tablas o vistas.
    Gestión de datos, escritura, edición... (CRUD)

Sin embargo, en ocasiones se puede escribir código SQL directamente por medio del ORM (en casos donde las queries son complejas). Conceptos que debemos tener en cuenta, como:

Migraciones: Scripts que describen cambios en la estructura de la base de datos, permitiendo versionarla y modificarla de forma controlada.

   - Semillas (Seeds): Datos iniciales que se insertan en la base de datos para pruebas o configuración inicial.

   - Modelos: Clases que representan tablas de la base de datos en el código orientado a objetos.

   - Consultas (Queries): Operaciones para recuperar, filtrar o manipular datos usando métodos del ORM en lugar de SQL directo.

- Relaciones: Conexiones entre modelos que reflejan las relaciones entre tablas (uno a uno, uno a muchos, muchos a muchos).

- Validaciones: Reglas definidas en los modelos para asegurar la integridad de los datos antes de guardarlos.

- Callbacks: Métodos que se ejecutan automáticamente en ciertos momentos del ciclo de vida de un objeto (antes o después de guardar, eliminar, etc.).
    
- Eager Loading: Técnica para cargar datos relacionados en una sola consulta, evitando el problema N+1.

- Transacciones: Operaciones que agrupan múltiples cambios en la base de datos, asegurando que se realicen todos o ninguno.

- Índices: Estructuras de la base de datos que mejoran la velocidad de las consultas, definidas a través del ORM.

- Herencia: Capacidad de los modelos de heredar atributos y comportamientos de otros modelos.

-   Migraciones reversibles: Migraciones que pueden deshacerse, permitiendo volver a un estado anterior de la base de datos.


continuaciòn