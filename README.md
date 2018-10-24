# 🧡 PIOCAMP 2018 | Taller de CSS desde cero 🧡

Hola Pionera !!! Desde ya me siento muy orgullosa de ti por tener esas ganas de aprender y esa linda dedicación. Esas son piezas fundamentales para ser una excelente desarrolladora. ¡ Sique así 😃 !

## ¿ Qué haremos ?

Haremos una página web sobre nosotras mismas 😊

## ¿ Qué aprenderemos ?

Aprenderemos sobre:
* Maquetación 
* Flexbox
* CSS Grid

## ¿ Qué debemos hacer para comenzar ?

1. Leer unas guías sobre Flexbox y CSSGrid.
2. Jugar para poder aplicar lo leído.
3. Clonar este repositorio.
4. Leer el paso a paso de este taller.

Ahora siiiii, ¿ estás lista ? 

¡ Empecémos !

# 💜 Mi primera página web con HTML y CSS 💜

### Tabla de contenidos:
1. [Guías sobre Flexbox y CSS Grid](#1-guías-sobre-flexbox-y-css-grid)
2. [Juegos sobre Flexbox y CSS Grid](#2-juegos-sobre-flexbox-y-css-grid)
3. [Después de clonar el repositorio...](#3-después-de-clonar-el-repositorio)
4. [Conozcamos la estructura de nuestra página web](#4-conozcamos-la-estructura-de-nuestra-página-web)
5. [Header](#5-header)
6. [Navbar](#6-navbar)
7. [About me - Section](#7-about-me---section)
8. [Tech - Section](#8-tech--section)
9. [Hobbies - Section](#9-hobbies---section)
10. [Footer](#10-footer)
11. [Reto](#11-reto)

## 1. Guías sobre Flexbox y CSS Grid

Unas guías que siempre me han salvado la vida y que hoy te quiero compartir, son:

* https://css-tricks.com/snippets/css/a-guide-to-flexbox/
* https://css-tricks.com/snippets/css/complete-guide-grid/

Espero te gusten y te sean útiles, no solo para hoy sino para el futuro.

## 2. Juegos sobre Flexbox y CSS Grid

Aquí te dejo los siguientes links para que juguemos un ratico:

* https://flexboxfroggy.com/#es
* https://cssgridgarden.com/#es

## 3. Después de clonar el repositorio...

Después de clonar el repositorio encontrarás dos carpetas: inicial y final. Tú comenzarás a escribir código en el `index.html` que dejé para ti en la carpeta inicial. Y porsupuesto, en la carpeta final está el resultado al que debemos llegar.

Para correr tu página, debes ir al navegador y poner la ruta en la que se encuentra tu proyecto. un ejemplo sería:

`file:///Users/user/Documents/PIOCAMP/workshop-css/inicial/index.html`

## 4. Conozcamos la estructura de nuestra página web

Aquí te muestro el resultado final de nuestra página !!! Eso sí, puedes escoger los colores, fotos y fuentes que más te gusten 🤗 

Encontrarás un header, un navbar, tres secciones y un footer. ¡ Trata de identifícalos !

<img src="./assets/layout.png" alt="layout"/>

## 5. Header

Antes de comenzar, es muy buena práctica que nuestro CSS tenga:
```
body {
    margin: 0;
    padding: 0;
}
```
Y ahora sí, para nuestro Header, el HTML es el siguiente:
```
<header>• PIOCAMP 2018 | CSS WORKSHOP •</header>
```
Y, en nuestro CSS tendremos:
```
header {
    background-color: #FB9495;
    color: white;
    padding: 4px;
    position: fixed;
    text-align: center;
    width: 100%;
    z-index: 3;            
}
```
Dónde:
* `background-color` nos dará el color de fondo.
* `color` le dará el color a nuestro texto.
* `padding` nos dará un margen interno. 
* `position: fixed` hará que nuestro header quede fijo y no se mueva por nada del mundo cuando hagamos scroll en la pantalla.
* `text-align: center` nos alineará nuestros textos de forma horizontal.
* `z-index: 3` hará que el header esté por encima del navbar que haremos a continuación y del background. El background por defecto tiene un z-index de 1 y de ahí comenzamos a contar, por eso el número 3. 

> Nota: Si te fijas, todas las propiedades están escritas en orden alfabético al igual que las clases. Tú puedes escribirlas en el orden que quieras. Sin embargo, escribir código en CSS en orden alfabético, nos permite tener un mayor orden y es más fácil llegar a las propiedades o clases si están en ese orden y así no tendremos que buscar en la inmensidad.

## 6. Navbar 

En nuestro HTML colocaremos lo siguiente:

```
<nav>
    <div class="nav-bottom">
        <h1> TU_NOMBRE_AQUÍ </h1>
    </div>
</nav>
```

Y, en nuestro CSS:

```
nav {
    background-color: white;
    box-shadow: 0 6px 6px rgba(0,0,0,0.23);
    padding-bottom: 10px;
    position: fixed;
    width: 100%;
    z-index: 2;
}
```
Dónde:
* `box-shadow` nos da esa sombrita y esa sensación de que está por encima como si fuera una hoja de papel.

Y el CSS de `h1` sería:

```
.nav-bottom h1 {
    color: #FB9495;
    font-family: 'Great Vibes', cursive;
    font-size: 40px;
    margin-top: 40px;
    margin-bottom: 10px;
    text-align: center;
}
```
Dónde:
* `font-family` es el tipo de letra y lo puedes escoger de Google Fonts. Cuando escojas tu letra, debes poner el link en la parte superior y ahí sí puedes hacer uso de la propiedad font-family.

Debajo del `h1` pondremos una lista con nuestras redes sociales o sitios de interés, algo así:
```
<ul>
    <li><a href="">• GitHub •</a></li>
    <li><a href="">• Instagram •</a></li>
    <li><a href="">• Twitter •</a></li>
    <li><a href="">• Medium •</a></li>
</ul>
```
En `href` debes poner los links, por ejemplo, en mi caso pondría `<li><a href="https://github.com/teffcode">• GitHub •</a></li>`

Y bueno, aquí entramos con la parte divertida. Un `ul` por defecto nos va a colocar todos los items con un puntico y uno debajo del otro, pero nosotros queremos modificar esto un poco. Queremos que la lista sea horizontal y para ello basta con poner `display: flex`, pero como van a estar muy juntitos, los separamos con `justify-content: space-evenly` y adicionalmente, le quitaremos a los items esos punticos con `list-style-type: none` y a los links les quitaremos el subrayado por defecto con `text-decoration: none;`.

El CSS quedaría así:

```
.nav-bottom  ul { 
    display: flex;
    font-size: 20px;
    justify-content: space-evenly;
    list-style-type: none;
    margin: 0;
    padding: 0;
}

.nav-bottom a {
    color: #333;
    text-decoration: none;
}

.nav-bottom a:hover {
    color: #FB9495;
}
```

## 7. About me - Section

Esta sección tendrá una imagen de fondo y la puedes descargar de https://www.freepik.com/ o de cualquier otro lugar que tenga imagenes gratis. Adicionalmente tendrá un título y una pequeña descripción acerca de nosotras.

Así, que nuestro HTML quedaría:
```
<section class="about-me-section text-center">
    <h2>About me:</h2>
    <p>
        I'm Software Developer <br/> 
        I live in Medellín <br/> 
        I like candy 
    </p>
</section>
```
Dónde `text-center` será una clase que usaremos mucho para centrar nuestros textos:
```
.text-center {
    text-align: center;
}
```
y `about-me-section` sería:

```
.about-me-section {
    align-items: center;
    background-image: url('./assets/about-me.jpg');
    background-position: right bottom;
    background-size: cover;
    display: flex;
    flex-direction: column;
    height: 380px;
    justify-content: flex-end;
    padding-bottom: 60px;
    width: 100%;
}
```
Dónde:
* `align-items: center` nos centrará los elementos de forma vertical si estamos utilizando flexbox.
* `background-image` será nuestra imagen de fondo y para colocar la ruta, te invito a que consultes sobre rutas absolutas y relativas.
* `background-position` nos ayuda a cuadrar nuestro background. En este caso, quería que se viera más el teclado que está ubicado en la esquina inferior derecha y por eso le coloqué `right bottom`. Puede que con la imagen que hayas escogido no necesites escribir esta línea de código.
* `background-size` nos permite decirle el tamaño que queremos del background. Si no le ponemos esta propiedad, la imagen estará en su tamaño original y se repetirá.
* `flex-direction` nos hubica los elemenos uno debajo del otro puesto que al poner `display: flex` todos los elementos se posicionan uno al lado del otro y en este caso no queremos ese efecto.
* `justify-content: flex-end` nos alineará nuestro contenido hasta la parte de abajo. Por esa razón le pondremos un `padding-bottom` para generar un poco de espacio abajo. 

> Nota: Debemos tener cuidado al colocar la propiedad `padding` puesto que esta nos aumenta el tamaño de nuestros elemenos. Entonces, ahí ya debemos jugar un poco tanto con el padding como con el width y height del elemento.

## 8. Tech- Section

Cosas que me encanten y los íconos. ¡ Soy fan de las páginas de íconos ! Aquí te dejo un enlace para que busques los que quieras: https://icons8.com/.

Si vas a usar `icons8` te recomiendo que sigas los pasos de la siguiente imagen:

<img src="./assets/icons8-instructions.png" alt="icons8-instructions"/>

También puedes buscar tus íconos en https://fontawesome.com.

En esta sección usaremos CSS Grid que es un sistema de layout que te permitirá ubicar los elementos en tu página de una forma muy fácil y nativa.

Nuestro HTML sería el siguiente:
```
<section class="tech-section text-center">
    <h2>I'm very passionate about:</h2>
    <div class="tech-section-books card">
        <p>Books</p>
        <img src="https://png.icons8.com/dusk/96/E4799B/book.png">
    </div>
    <div class="tech-section-courses card">
        <p>Courses</p>
        <img src="https://png.icons8.com/dusk/96/E4799B/windows-client.png">
    </div>
    <div class="tech-section-develop card">
        <p>Develop</p>
        <img src="https://png.icons8.com/dusk/96/E4799B/code-file.png">
    </div>
</section>
```
Y el CSS:
```
.card {
    border-radius: 15px;
    box-shadow: 0 10px 20px rgba(0,0,0,0.19), 0 6px 6px rgba(0,0,0,0.23);
    grid-row: 2;
    height: 85%;
    justify-self: center;
    width: 80%;
}

.card:hover {
    transform: scale(1.05);
}

.tech-section {
    background-color: white;
    display: grid;
    grid-template-columns: repeat(5, 1fr);
    grid-template-rows: 100px auto;
    height: 300px;
    width: 100%;
}

.tech-section  h2 {
    grid-column: 2 / 5;
    line-height: 2.5;
}

.tech-section-books {
    background-color: #FDF1B2;
    grid-column: 2 / 3;
}

.tech-section-courses {
    background-color: #FEEAE9;
    grid-column: 3 / 4;
}

.tech-section-develop {
    background-color: #FDF1B2;
    grid-column: 4 / 5;
}
```

## 9. Hobbies - Section

Esta sección es muy similar a la anterior. Así que, ¡ trata de hacerla ! Si tienes dudas, pregúntanos 😉

## 10. Footer

Esta es la última parte de nuestra página 🎉 Wiiii 🎉

El HTML es muy simple:

```
<footer>• Site by TU_NOMBRE_AQUÍ •</footer>
```
Y en el CSS tendremos un color de fondo, un color del texto, tamaños y una alineación:
```
footer {
    background-color: #FB9495;
    color: white;
    padding: 4px;
    text-align: center;
    width: 100%;
}
```

## 11. Reto

Este es un reto personal y todo con el fin de mejorar tus _skills_. Y la idea esssss: Hacer el `responsive` de esta página 😱  

Si tienes dudas, puedes consultar los siguientes enlaces:

* https://developer.mozilla.org/es/docs/Web_Development/Mobile/Dise%C3%B1o_responsivo
* https://developers.google.com/web/fundamentals/design-and-ux/responsive/
* https://www.w3schools.com/html/html_responsive.asp




