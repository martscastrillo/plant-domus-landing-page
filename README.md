# Proyecto final de módulo - HTML Y CSS

#### Por Marta Castrillo

### Funcionalidades del proyecto

Es una web con una única página preparada para su uso responsive.

### Acceso al proyecto

El proyecto está preparado para poder levantarlo con el comando `npm start` Si quisieras hacerlo pero algún motivo no dispones de la carpeta **node_modules** antes de realizar el proceso de levantarlo, deberás instalarlo con el comando `npm install`

Una vez hechos estos pasos uno o los dos podrás tener acceso al proyecto en funcionamiento.

### Tecnologías utilizadas

Tienes a disposición en el proyecto, las dependencias necesarias para el empleo de SCSS. Para el uso correcto de este sistema, he empleado partials, para facilitar y aligerar los archivos de código individuales, tanto en html como en scss.

### Desarrollo del código

El proyecto, por ser una web funciona básicamente con html y css (más luego toda la gestión de las dependencias que se encargan nuestros amigos de npm)
La página consta de:

- Una imagen principal que ocupa de incio todo el alto del viewport, inlcuyendo un menú hamburguesa que va a estar presente a lo largo de toda la navegación en por la página, consta tambien de unos textos (el principal con una sutil sombra ) así como una flecha que nos hace navegar hacia una sección concreta de nuestra página.
- Un segundo bloque que consta de un titulo principal, uno secundario extra y un párrafo, junto con un botón. El botón al pasar el cursor por encima, realiza un cambio de posicion y un cambio en el diseño de los colores, usando `:hover` para que no se fuera de una manera brusca y violenta he aplicado con `:not(:hover)` un `transition` del mismo valor que tiene inicialmente la propiedad, para que igual que viene, se va.
- Un tercer bloque que consta de un titulo y unos articulos, estos están diseñados con partials por parámetros desde html, para en caso de cambiar o añadir, que se produzca el proceso de la manera más rápida y cómoda posible. También dispone de un botón, este, como el anterior, cuando se pasa el cursor por encima, realiza un cambio de, en este caso de la escala y un cambio en el diseño de los colores, aplicando de nuevo `:not(:hover)` para suavizar el movimiento con una `transition`
- Un cuarto bloque o footer, tiene tres bloques de texto repartidos según el dispositivo. Todos los enlaces del footer tienen aplicada la propiedad `:hover` para que cuando se pase el cursor sobre ellos cambie a uno de los colores corporativos, al hacer click nos dirige a una página dada, pero por añadirle `target="_blank"` nos manda a la página abriendo una nueva pestaña, lo que hace que el lector no se aleje de nuestro contacto. La flecha del footer , además de una sutil sombra, tiene una pequeña y sutil animación, con la propieddad infinita, para que no solo se cargue al hacerlo la página, sino que la animación sea visual durante todo el proceso.
  `animation: bounce 2s ease infinite` donde _bounce_ es el nombre que le he dado a la animación (más adelante necesito aplicarle a esa animación unos keyframes) _2s_ es el tiempo que dura la animación _ease_ es la curva de la velocidad de la animación e _infinite_ supone el tiempo que perdura esa animación en el tiempo. Como he indicado posteriormente encontramos los keyframes de nuestra animation, ahí tenemos `50% { transform: translateY(-30px); }` donde el 50% es la cifra con la que se indica desde 0% hasta 100% por ejemplo, al tenerlo en el 50% la aniumacion no va "terminar" ni "empezar" nunca, lo que la hace mucho más fluida.
  Además del hover, los enlaces de nuestro footer tienen aplicados un title a modo tip tool donde te da una pista de dónde te lleva ese enlace.

Todas estas caracteristicas han sido adaptadas para que suponga de una buena experiencia por parte del usuario, siendo todo lo responsive posible, tomando como referencia 3 tipos de viewports genéricos 320px, 768px y 1280px en cada caso, de modo que se han ido aplicando las media queries correspondientes a cada tipo de viewport, tomando siempre como punto de partida **mobile first**

Por otro lado, se han dispuesto hojas de reset para el proyecto, para una serie de caracteristicas evitarlas y partir de cero. También se han usado variables, para tanto el uso de colores como tipografías más repetidas a lo largo del proceso.
