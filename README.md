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