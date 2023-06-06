# DayDash PHP
Este proyecto consiste en un panel dashboard escrito en php, el proyecto sera de una unica pagina en la que ocurrira  todo.
## Pantalla principal
La pantalla principal tendra un header con una foto de perfil a la izquierda seguido de un boton + que permite entrar al menu de los nodos (que permite crear o eliminar nodos), añadir nodos a la pagina actual (instancias de un nodo). Un mensaje del dia en el centro y informacion sobre el tiempo a la derecha.
Debajo del header hay una barra buscadora multiusos. Con un efecto similar al de k-runner en linux permite: Hacer operaciones matematicas, lanzar busquedas en google, y ejecutar comandos de DayDash.
Debajo de la barra de buscador habra un dock a la derecha con layouts. Un layout no es mas que una organizacion de los nodos para presentarlos de forma virtual. Un layout almacena el ancho, y alto en bloques. Asi como la posicion de los nodos.
Los nodos van a la izquierda del dock. Consiste en una tabla. Los nodos pueden ser links (si tienen un link asignado) o informativos si el link es null en la base de datos.
## Nodos:
Los nodos son elementos que se muestran en layouts o pantallas. Cuando añades un nodo a una screen, se crea una entrada en la tabla node_screen, esta entrada en node_screen se interpreta como una instancia del nodo original. La informacion del nodo esta en el propio nodo de forma que si se actualiza se actualiza en todos pero el tamaño puede variar segun la presentacion.
# Diseño
Se usará tailwind.css para el css general
# Estructura de directorios
Se basara el proyecto en una estructura por componentes y screens.

    DayDashPHP/
    ├── components/
    │   ├── Header.php
    │   ├── Sidebar.php
    │   ├── Footer.php
    │   ├── ...
    ├── macrocomponents/
    │   ├── Carousel.php
    │   ├── Modal.php
    │   ├── ...
    ├── pages/
    │   ├── Home.php
    │   ├── About.php
    │   ├── Contact.php
    │   ├── ...
    ├── resources/
    │   ├── css/
    │   │   ├── style.css
    │   │   ├── ...
    │   ├── js/
    │   │   ├── script.js
    │   │   ├── ...
    │   ├── images/
    │   │   ├── logo.png
    │   │   ├── ...
    │   ├── uploads/
    │   │   ├── file1.jpg
    │   │   ├── ...
    ├── config.php
    ├── includes/
    │   ├── functions.php
    ├── cronjob.php
    ├── index.php
    └── README.md


