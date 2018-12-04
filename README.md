# NINFORMATICS

Este sitio nació como proyecto final para la materia de **Desarrollo de Aplicaciones Web**. Este proyecto es un blog de noticias relacionadas con el mundo de los videojuegos, publicando avances, notas, lanzamientos, entre otros contenidos, teniendo en mente las fuentes realmente confiables, es decir, cero rumores.

# Pongámonos en marcha
Para copiar este archivo necesitaremos de una consola Linux, en ella tenemos que abrir una carpeta donde se alojará el proyecto.
En nuestra consola pondremos:
>$ mkdir ((nombre-que-quieras))
- Ahora necesitamos alojarnos 
> $ cd ((nombre-que-elegiste))
- en esa carpeta que acabamos de crear y una vez dentro ejecutar un ambiente virtual en donde correrá nuestro proyecto, este se abrirá de esta manera:
>$ python3 -m venv ((nombre-que-quieras))
- Ahora ya debería haberse creado nuestro ambiente virtual, ahora solo queda activarla.
> $ source ((nombre-de-tu-ambiente))/bin/activate
- Con eso nos encontraremos dentro de nuestro ambiente virtual, lo siguiente es conseguirnos las herramientas necesarias para trabajar con el y nuestro proyecto, que sería Django. En la consola se colocará lo siguiente:
> $ pip install -U pip
> $ pip install django
- Una vez hecho esto ya podemos trabajar en el proyecto, ahora viene lo bueno, para "jalar" el proyecto y trabajar con el tendremos que utilizar:
> $ git pull https://github.com/CoAnheru/proyecto
- Enseguida se comenzará a descargar el proyecto, una vez se descargue accederemos a el con:
> $ cd proyecto
- Ahora nos encontraremos en el proyecto y ya podemos trabajar sobre el y editar su contenido
## Pre-requisitos:
Para trabajar en este proyecto se necesita un ambiente linux debido a que trabajaremos con su consola, es opcional un editor de texto para trabajar de manera más sencilla. También se requiere de una cuenta de github y opcionalmente una cuenta de pythonanywhere si es que se quieren alojar los cambios hechos a este proyecto en linea.


# Estructura

La estructura de este proyecto está basada en MVC (Modelo-Vista-Controlador) y fue programado utilizando el framework Django utilizando Python como lenguaje de codificación. 
En conjunto se utiliza CSS y Bootstrap para el diseño del sitio, 
además de plantillas en html. Para realizarlo se utilizó una máquina virtual que simulaba linux lite
# Probando... probando...
Para ver nuestro proyecto podemos abrir una consola aparte de la que estamos utilizando para movernos entre los directorios, o puede ser en la misma, pero la primera opción resulta más comoda ya que trabajamos de manera más rápida, entonces, en nuestra consola entraremos a la carpeta donde se encuentre nuestro proyecto, activamos nuestro entorno virtual y nos metemos al proyecto.
> cd ((nombre_carpeta_de_proyecto))
> source ((nombre_ambiente_virtual))/bin/activate
> cd proyecto
- Ahora probemos ejecutando el servidor.
> python manage.py runserver
- Si el servidor se ejecuta correctamente entonces solo restará abrir nuestro navegador y dirigirnos a localhost:8000 o a http://127.0.0.1:8000/ y veremos nuestro proyecto en acción.
Lo siguiente sería entrar a los posts, ver los comentarios, hacernos una cuenta, ver que restricciones tiene esa cuenta y compararla con una cuenta de administrador. Recordemos que la cuenta de administrador se hace con:
> python manage.py createsuperuser
- si ejecutamos eso nos irá pidiendo ciertos datos, ese será nuestro login de administrador, ahora intentemos logearnos como administrador en nuestro proyecto con las credenciales que acabamos de capturar, ¿notas la diferencia?
- Estando como administrador podemos agregar posts, editarlos, aprobarlos y moderar comentarios, cosa que un usuario común no puede hacer, notarás eso cuando veas la cantidad de botones que hay por ahí.
## Oye oye, pero, ¿como que ponerlo en línea?
Oh, cierto, con pythonanywhere.com podemos alojar el proyecto en línea por un cierto tiempo (a menos que paguemos, lo normal, ¿no?) pythonanywhere actuará como una consola con la cual podremos hacer git pull y ver los cambios en tiempo real. Para eso necesitaremos registrarnos en esa página.
Una vez hecho eso, iremos por un token. Tenemos que hacer click en "*Account*" y luego "*API token*", una vez ahí le damos clic al botón de solicitar API token. Ahora entramos a "$bash", que vendría a ser la consola.
Estando dentro de la consola colocaremos esto:
> $ pip3 install --user pythonanywhere
- ¿Te parece conocido?, sí, estamos configurando la máquina para el proyecto. Una vez termine la instalación haremos que pythonanywhere se configure automaticamente a nuestro proyecto con esto:
> $ pa_autoconfigure_django.py https://github.com/CoAnheru/proyecto.git
- Esto tardará un rato, pero una vez termine nuestro proyecto ya estará alojado en pythonanywhere, ¡recuerda hacer un nuevo superusuario! los usuarios que hacemos y los posts no se guardan al hacer pull o push, esto se debe a que la base de datos que se encuentra en pythonanywhere es otra. Una vez tengamos nuestro super usuario
- > $ python manage.py createsuperuser
- podremos entrar como administrador y agregar posts al proyecto, se ve bien ¿no?.
- Recuerda que si quieres guardar los cambios y que se reflejen en python anywhere hay que hacer pull y push desde esta consola. Oh y algo muy importante, recuerda refrescar la web con el botón "Reload" que se encuentra en la pestaña de red, esto actualizará la página y mostrará los cambios.

# Autores del proyecto
El proyecto ha sido desarrollado por los integrantes del grupo 351 de la licenciatura en informática de UABC
- Miguel Angel Raygoza Cortes
- Victor Manuel García Guzman
- Daniel Rodriguez Moreno
- Christopher Osuna Barrera

## Soporte

Muchas gracias al profesor Jose Carlos Gallegos Mariscal por ayudarnos con su código, nos sirvió muchísimo para lo que queríamos hacer, realmente fue la base del proyecto. También agradecer  a William S. Vincent por su código de signup.

