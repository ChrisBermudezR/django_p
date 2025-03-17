# Entendiendo la arquitectura de Django

¿Qué es el modelo en MVT (Model, View, Template)?

El modelo es la parte de los datos:

    Guarda y procesa los datos.
    Contiene la lógica del negocio, como una calculadora que suma 2 más 2.

Modelo (Model)
El modelo es responsable de la lógica de negocio y la gestión de los datos. Define la estructura de la base de datos y las relaciones entre los datos. En Django, los modelos se definen como clases en Python y se mapean a tablas en la base de datos.

Funciones del modelo:

Guarda y procesa los datos.
Contiene la lógica del negocio.

¿Qué es la vista en MTV?

La vista actúa como un conector:

    Accede y dirige los datos.
    Controla el flujo de peticiones y respuestas.
    Verifica permisos y realiza comprobaciones necesarias.

Vista (View)
La vista actúa como un intermediario entre el modelo y el template. Gestiona las solicitudes del usuario, obtiene datos del modelo y los pasa al template para su presentación. También maneja la lógica de control, como la verificación de permisos y la gestión del flujo de peticiones y respuestas.

Funciones de la vista:

Accede y dirige los datos.
Controla el flujo de peticiones y respuestas.
Verifica permisos y realiza comprobaciones necesarias.

¿Qué es el template en MTV?

El template maneja la parte gráfica:

    Usa HTML y CSS para mostrar los datos.
    Por ejemplo, muestra una lista de zapatos almacenada en el modelo.

Template
El template es responsable de la presentación de los datos. Utiliza HTML y CSS para mostrar los datos al usuario. Los templates en Django son archivos HTML que pueden contener etiquetas de template para mostrar datos dinámicos.

¿Cómo interactúan modelo, vista y template?

El flujo de datos es el siguiente:

    El modelo pasa datos a la vista en un array.
    La vista pasa esos datos al template en un contexto.
    El template muestra los datos gráficos.

En sentido contrario:

    Un usuario busca en el template.
    La vista recibe la búsqueda y consulta al modelo.
    El modelo devuelve los resultados a la vista.
    La vista envía los datos al template para mostrarlos.

Nota: No debe haber conexión directa entre template y model. Siempre usa la vista para asegurar verificaciones y permisos.

https://docs.djangoproject.com/en/5.0/glossary/#term-MTV