¡Perfecto\! Vamos a enriquecer esa guía. He integrado las propiedades que mencionaste (`border`, `border-radius`, `outline`) y otras propiedades básicas esenciales (`visibility`, `opacity`, `cursor`, `text-transform`, `object-fit`) directamente en la estructura que ya tenías, detallándolas un poco más.

Aquí tienes la guía actualizada y más completa:

-----

### 1\. 🏁 Introducción a CSS

Breve historia, para qué sirve y cómo se relaciona con HTML. Sintaxis básica.

  * **¿Qué es CSS?** (Cascading Style Sheets): Es el lenguaje que usamos para definir la **presentación visual** y el estilo de un documento HTML.
  * **Historia y evolución de CSS**: Nació para **separar el contenido (HTML) de la presentación (CSS)**. Ha evolucionado de CSS1 a CSS3 y ahora se desarrolla en "módulos" (Flexbox, Grid, etc.).
  * **Relación entre HTML y CSS**: HTML define la **estructura** y el contenido (los "ladrillos"), mientras que CSS define el **aspecto** (la "pintura y decoración").
  * **Sintaxis básica de CSS**:
    `selector { propiedad: valor; }`
      * **Selector**: El elemento HTML a estilizar (ej. `h1`, `.menu`, `#logo`).
      * **Propiedad**: El atributo que quieres cambiar (ej. `color`, `font-size`).
      * **Valor**: El ajuste para esa propiedad (ej. `blue`, `20px`).

-----

### 2\. 🚀 Primeros pasos

Cómo incluir CSS en una página, selectores básicos y comentarios.

  * **Formas de incluir CSS**:
      * **Externa (Recomendada)**: En un archivo `.css` separado, vinculado con `<link rel="stylesheet" href="style.css">` en el `<head>`.
      * **Interna**: Dentro de una etiqueta `<style>` en el `<head>` del HTML.
      * **En línea**: Usando el atributo `style` en una etiqueta HTML (ej. `<p style="color: red;">`). (Evitar en lo posible).
  * **Selectores básicos**:
      * **Por etiqueta**: `p { ... }` (selecciona todos los `<p>`).
      * **Por clase**: `.mi-clase { ... }` (selecciona todos los `class="mi-clase"`).
      * **Por id**: `#mi-id { ... }` (selecciona el *único* `id="mi-id"`).
  * **Comentarios en CSS**: `/* Esto es un comentario */`

-----

### 3\. ✍️ Propiedades de texto

Modificar color, tipografía, tamaño, peso, estilo, alineación y espaciado del texto.

  * **Color de texto**: `color` (ej. `color: #333;`).
  * **Tipografía**:
      * `font-family`: Define la familia de la fuente (ej. `font-family: Arial, sans-serif;`).
      * `font-size`: Define el tamaño (ej. `font-size: 16px;`).
      * `font-weight`: Define el grosor (ej. `font-weight: bold;` o `700`).
      * `font-style`: Define el estilo (ej. `font-style: italic;`).
  * **Alineación y espaciado**:
      * `text-align`: Alineación horizontal (`left`, `center`, `right`).
      * `line-height`: Altura de línea (interlineado).
      * `letter-spacing`: Espacio entre letras.
      * `word-spacing`: Espacio entre palabras.
  * **Decoración y transformación**:
      * `text-decoration`: Añade o quita decoración (ej. `underline`, o `none` para quitar el subrayado de los enlaces).
      * `text-transform`: Cambia las mayúsculas/minúsculas (`uppercase`, `lowercase`, `capitalize`).
      * `text-indent`: Aplica sangría a la primera línea de un texto.

-----

### 4\. 🎨 Fondos y bordes

Personalizar el fondo y los bordes de los elementos, incluyendo degradados y sombras.

  * **Color y degradados de fondo**:
      * `background-color`: Color de fondo sólido.
      * `background-image`: Imagen de fondo (con `url('...')`) o un degradado (ej. `linear-gradient(...)`).
      * `background-repeat`: Controla si la imagen se repite (`no-repeat`, `repeat`).
      * `background-size`: Tamaño de la imagen de fondo (`cover`, `contain`).
  * **Bordes**:
      * `border`: Propiedad "shorthand" (atajo) para definir los tres valores a la vez (ej. `border: 2px solid #ccc;`).
      * `border-width`: Grosor del borde (ej. `2px`).
      * `border-style`: Estilo del borde (`solid`, `dashed`, `dotted`).
      * `border-color`: Color del borde.
      * **`border-radius`**: **Esencial**. Se usa para redondear las esquinas de un elemento (ej. `border-radius: 8px;` para esquinas suaves, o `border-radius: 50%;` para crear un círculo).
  * **Contorno (Outline)**:
      * **`outline`**: Similar a `border`, pero con dos diferencias clave:
        1.  **No ocupa espacio**: Se dibuja *fuera* del Box Model, por lo que no empuja a otros elementos.
        2.  Se usa a menudo para accesibilidad (ej. para resaltar un elemento en `:focus`).
      * Sintaxis: `outline: 2px solid blue;`
  * **Sombra**:
      * `box-shadow`: Añade una sombra a la "caja" del elemento.
      * `text-shadow`: Añade una sombra directamente al texto.

-----

### 5\. 📦 Modelo de caja (Box Model)

Entender cómo se calcula el espacio de los elementos: margen, relleno, ancho, alto y desbordamiento.

  * **Margen (Margin)**: `margin`. El espacio **exterior** de la caja, que la separa de otros elementos.
  * **Relleno (Padding)**: `padding`. El espacio **interior** de la caja, entre el borde y el contenido.
  * **Ancho y alto**: `width`, `height`. Definen el tamaño del área de *contenido*.
  * **Propiedad clave**: `box-sizing: border-box;`. Por defecto, `width` y `height` solo miden el contenido. Si usas `border-box`, el `width` que definas incluirá el `padding` y el `border`, haciendo las matemáticas de diseño mucho más fáciles.
  * **Desbordamiento**: `overflow`. Qué hacer si el contenido es más grande que la caja (`hidden` lo oculta, `scroll` o `auto` añaden barras de desplazamiento).

-----

### 6\. 📏 Unidades de medida

Diferencias entre unidades absolutas y relativas.

  * **Unidades absolutas**: Tienen un tamaño fijo.
      * `px`: Píxeles. La más común, pero menos flexible.
  * **Unidades relativas**: Su tamaño depende de otro valor (¡mejores para responsive\!).
      * `%`: Relativo al elemento padre.
      * `em`: Relativo al `font-size` del elemento *padre*.
      * **`rem` (Root EM)**: Relativo al `font-size` del `<html>` (la raíz). **Muy recomendada** para tipografía y espaciados.
      * `vw` (Viewport Width): 1% del ancho de la ventana.
      * `vh` (Viewport Height): 1% del alto de la ventana.

-----

### 7\. 📍 Posicionamiento y display

Cómo se colocan los elementos en la página.

  * **Tipos de `display`**: Controla cómo se renderiza la caja.
      * `block`: Ocupa todo el ancho disponible y se apila verticalmente (ej. `<div>`, `<p>`).
      * `inline`: Ocupa solo el espacio de su contenido y fluye con el texto (ej. `<span>`, `<a>`). Ignora `width` y `height`.
      * `inline-block`: Como `inline` (fluye), pero respeta `width` y `height`.
      * `none`: Oculta el elemento y lo saca del flujo (como si no existiera).
  * **Posicionamiento (`position`)**:
      * `static`: Comportamiento normal por defecto.
      * `relative`: Se puede mover *relativo* a su posición original (con `top`, `bottom`, `left`, `right`).
      * `absolute`: Se saca del flujo y se posiciona relativo a su ancestro posicionado más cercano.
      * `fixed`: Se posiciona relativo a la ventana. No se mueve al hacer scroll.
      * `sticky`: Mezcla de `relative` y `fixed`. Se "pega" al llegar a un punto del scroll.
  * **Capas y Visibilidad**:
      * `z-index`: Define qué elemento posicionado está "encima" de otro (un número más alto está más al frente).
      * `visibility`: Permite ocultar un elemento.
          * `visibility: hidden;`: Oculta el elemento, pero **sigue ocupando su espacio** (a diferencia de `display: none`).
          * `visibility: visible;`: Lo vuelve a mostrar.
      * `opacity`: Define la transparencia de un elemento (de `0.0` transparente a `1.0` opaco).

-----

### 8\. 🖱️ Listas, tablas, formularios e imágenes

Estilizar elementos comunes para mejorar su apariencia.

  * **Estilizar listas**: `list-style` (o `list-style-type: none;` para quitar los puntos/viñetas).
  * **Estilizar tablas**: `border-collapse: collapse;` (para unir los bordes de las celdas).
  * **Estilizar formularios**: Se estilan `input`, `button`, `textarea`, etc.
  * **Cursor**: `cursor`. Cambia el puntero del mouse al pasar sobre un elemento (ej. `cursor: pointer;` para simular un enlace, `cursor: not-allowed;` para acciones deshabilitadas).
  * **Imágenes**:
      * `object-fit`: Define cómo debe una imagen (u otro medio) ajustarse a su contenedor si tiene un `width` y `height` fijos.
          * `object-fit: cover;`: (El más útil) Escala la imagen para que rellene el contenedor, recortando lo que sobre (sin distorsionar).
          * `object-fit: contain;`: Escala la imagen para que quepa entera, pudiendo dejar bandas vacías.

-----

### 9\. 🎯 Selectores avanzados y pseudo-clases

Seleccionar elementos de forma avanzada y aplicar estilos según el estado o posición.

  * **Selectores combinadores**:
      * Descendencia: `div p` (un `p` dentro de un `div`).
      * Hijo directo: `div > p` (un `p` que es hijo *directo* de `div`).
  * **Pseudo-clases (Estado)**:
      * `:hover`: Cuando el cursor está encima.
      * `:active`: Cuando se hace clic.
      * `:focus`: Cuando se selecciona con el teclado (importante para accesibilidad).
  * **Pseudo-clases (Estructurales)**:
      * `:first-child` / `:last-child`: El primer o último hijo.
      * `:nth-child(n)`: Selecciona hijos específicos (ej. `:nth-child(even)` para filas pares).
  * **Pseudo-elementos (Crean elementos "virtuales")**:
      * `::before`: Inserta contenido *antes* del contenido del elemento.
      * `::after`: Inserta contenido *después* del contenido del elemento.

-----

### 10\. 🥇 Especificidad y herencia

Cómo CSS decide qué estilos aplicar y cómo se heredan los estilos entre elementos.

  * **Especificidad**: Un sistema de "puntos" para decidir qué regla gana si hay un conflicto.
      * (Baja) Etiquetas (`p`) \< Clases (`.clase`) \< IDs (`#id`) (Alta).
      * Un estilo en línea (atributo `style`) casi siempre gana.
      * `!important` fuerza la aplicación de un estilo (¡evitar si es posible\!).
  * **Herencia**: Algunas propiedades (como `color` y `font-family`) se heredan de padres a hijos automáticamente. Otras (como `border` y `padding`) no.

-----

### 11\. ➡️ Flexbox

Sistema moderno para organizar y alinear elementos en **una sola dimensión** (fila o columna). Esencial para la maquetación.

  * **Activar**: `display: flex` (en el contenedor padre).
  * **Propiedades del Contenedor (Padre)**:
      * `flex-direction`: Dirección de los hijos (`row` o `column`).
      * `justify-content`: Alineación en el eje principal (horizontal si es `row`).
      * `align-items`: Alineación en el eje secundario (vertical si es `row`).
      * `flex-wrap: wrap;`: Permite que los hijos "salten" a la siguiente línea si no caben.
  * **Propiedades de los Hijos (Items)**:
      * `flex-grow`, `flex-shrink`, `flex-basis`: Definen cómo un hijo crece o se encoge.
      * `order`: Cambia el orden visual de un hijo.

-----

### 12\. 🏁 CSS Grid

Sistema avanzado para crear diseños de **dos dimensiones** (filas y columnas) de forma sencilla.

  * **Activar**: `display: grid` (en el contenedor padre).
  * **Propiedades del Contenedor (Padre)**:
      * `grid-template-columns`: Define las columnas (ej. `repeat(3, 1fr)` para 3 columnas iguales).
      * `grid-template-rows`: Define las filas.
      * `gap`: Define el espacio de separación entre celdas.
  * **Propiedades de los Hijos (Items)**:
      * `grid-column`, `grid-row`: Definen dónde empieza y termina un hijo en la cuadrícula.

-----

### 13\. 💫 Transiciones y animaciones

Agregar efectos visuales y animaciones a los elementos de la página.

  * **Transformaciones**: `transform`. Permite mover (`translate`), escalar (`scale`), rotar (`rotate`) y sesgar (`skew`) elementos sin afectar a los demás.
  * **Transiciones**: `transition`. Anima suavemente el cambio de una propiedad (ej. en un `:hover`).
      * `transition: background-color 0.3s ease;`
  * **Animaciones**: `animation` y `@keyframes`. Para animaciones complejas y continuas, se definen los "fotogramas clave" con `@keyframes`.

-----

### 14\. 📱 Diseño adaptable (Responsive Design)

Hacer que la web se vea bien en cualquier dispositivo usando media queries y buenas prácticas.

  * **¿Qué es?**: La práctica de hacer que el diseño se "adapte" al tamaño de la pantalla.
  * **Meta Viewport**: **Esencial**. Añadir en el `<head>` del HTML:
    `<meta name="viewport" content="width=device-width, initial-scale=1.0">`
  * **Media Queries**: Permiten aplicar estilos CSS *solo* si se cumple una condición (como el ancho de la pantalla).
      * **Enfoque "Mobile-First" (Recomendado)**: Se diseña primero para móvil, y luego se usa `min-width` para añadir estilos en pantallas más grandes.
    <!-- end list -->
    ```css
    /* Estilos base (Móvil) */
    .contenedor { width: 100%; }

    /* Estilos para pantallas de 768px o más (Tablets) */
    @media (min-width: 768px) {
      .contenedor { width: 750px; }
    }
    ```
