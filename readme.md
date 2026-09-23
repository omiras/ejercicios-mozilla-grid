# Ejercicios de CSS Grid y Flexbox

En estos ejercicios organizarás elementos con **CSS Grid** y, en los dos últimos, también con **Flexbox**. Los archivos HTML ya contienen el contenido y parte de los estilos. Tu tarea es completar la distribución sin rehacer la página.

## Antes de empezar

Deberías conocer las reglas y clases CSS. Aquí practicarás columnas, filas, separación, colocación de elementos y distribución flexible. Para `grid1b.html` también necesitarás entender una consulta de medios (`@media`).

1. Abre el HTML del ejercicio en el navegador y en tu editor.
2. Localiza el bloque `<style>` y observa qué reglas ya están escritas.
3. Compara la página con la imagen o demostración correspondiente.
4. Haz un cambio pequeño, guarda y recarga el navegador. Comprueba el resultado antes de continuar.

No necesitas instalar nada ni usar JavaScript. Conserva los elementos HTML y las fotografías que trae cada ejercicio. Las imágenes `disseny*.png` y `diseeny2.png` muestran resultados esperados.

## 1. Primera cuadrícula — `grid1.html`

**Objetivo:** distribuir automáticamente las cuatro cajas en tres columnas iguales, con espacio entre columnas y filas. La cuarta caja debe iniciar la segunda fila.

![Resultado esperado de grid1](disseny1.png)

**Guía:** localiza el contenedor `.grid`. Investiga cómo convertirlo en una cuadrícula, cómo definir columnas del mismo ancho y cómo dejar espacio entre celdas. Resuelve primero las columnas y después la separación.

**Comprueba:** las tres primeras cajas están en una fila; «Four» aparece debajo de «One»; las columnas tienen el mismo ancho. Puedes añadir temporalmente una quinta caja para observar la colocación automática y retirarla al terminar.

<details>
<summary>Pista</summary>

Las columnas se definen en el contenedor. La unidad `fr` reparte el espacio disponible.

</details>

## 2. Columnas de distinto tamaño — `grid1b.html`

**Objetivo:** mostrar las citas en una columna en ventanas estrechas y, desde 600 px, en tres columnas. La central debe ser el doble de ancha que cada lateral.

[Ver la demostración enlazada en el HTML](https://oscarm.tinytake.com/df/172ed59/thumbnail?type=attachments&version_no=0&file_version_no=0&thumbnail_size=preview)

**Guía:** examina las reglas de `main` y la consulta `@media` existente. Prueba primero la página por debajo de 600 px. Después amplía la ventana e investiga cómo expresar proporciones entre columnas sin fijar su ancho en píxeles.

**Comprueba:** el cambio de disposición ocurre al llegar a 600 px; la columna central es aproximadamente el doble de ancha; las citas mantienen su orden.

<details>
<summary>Pista</summary>

La consulta de medios ya indica *cuándo* cambia el diseño. Revisa cómo definir el tamaño relativo de las columnas con `fr`.

</details>

## 3. Elementos que ocupan varias celdas — `grid2.html`

**Objetivo:** colocar las dos cajas en la cuadrícula de cuatro columnas y tres filas ya definida. Ambas deben abarcar varias celdas y solaparse como en la imagen.

![Resultado esperado de grid2](diseeny2.png)

**Guía:** identifica las filas y columnas existentes. Observa dónde comienza y termina cada caja en la referencia. Investiga cómo situar un elemento entre líneas de fila y columna. Trabaja con una caja cada vez.

**Comprueba:** «One» ocupa la zona superior izquierda; «Two» empieza más a la derecha y más abajo; ambas se superponen parcialmente.

<details>
<summary>Pista</summary>

Las líneas de Grid delimitan las celdas. Para abarcar varias, una caja necesita una línea inicial y otra final en cada dirección.

</details>

## 4. Colocación de cuatro elementos — `grid3.html`

**Objetivo:** reproducir la disposición de la imagen usando la cuadrícula de dos columnas ya preparada.

![Resultado esperado de grid3](disseny3.png)

**Guía:** dibuja las filas y columnas en papel. Decide qué zona ocupa cada caja y cuál queda vacía. Investiga cómo nombrar zonas de una cuadrícula y asignarlas a los elementos con las clases `.one`, `.two`, `.three` y `.four`.

**Comprueba:** «One» ocupa toda la primera fila; «Two» y «Three» comparten la segunda; «Four» queda a la derecha en la tercera, con un hueco a su izquierda.

<details>
<summary>Pista</summary>

Consulta `grid-template-areas` y `grid-area`. Piensa en los nombres de las zonas antes de escribir las reglas.

</details>

## 5. Tarjetas y etiquetas — `grid4.html`

**Objetivo:** organizar las tarjetas de fotografías en tres columnas con Grid y distribuir las etiquetas de cada tarjeta en filas centradas con Flexbox.

![Resultado esperado de grid4](disseny4.png)

**Guía:** identifica el elemento que contiene todas las tarjetas y el que contiene las etiquetas de una tarjeta. Resuelve primero la cuadrícula de tarjetas. Después consigue que las etiquetas puedan pasar a otra línea y queden centradas. No necesitas cambiar el HTML.

**Comprueba:** hay tres tarjetas en la primera fila y una en la segunda; las fotos mantienen su recorte; las etiquetas forman varias filas cuando hace falta y se centran bajo cada foto.

<details>
<summary>Pista</summary>

Grid organiza las tarjetas en filas y columnas. Para las etiquetas, investiga qué propiedad de Flexbox permite continuar en otra fila.

</details>

## 6. Tablero y teclado — `grid5-y-flex.html`

Este archivo contiene **dos ejercicios** en sus comentarios CSS. Resuélvelos por separado.

[Ver la demostración enlazada en el HTML](https://oscarm.tinytake.com/df/172e2ef/thumbnail?type=attachments&version_no=0&file_version_no=0&thumbnail_size=preview)

### Parte 1: tablero con Grid

**Objetivo:** organizar las 30 casillas de `.board` en exactamente seis filas y cinco columnas. El HTML indica una altura de 62 px para las casillas.

**Guía:** cuenta las casillas y relaciona el total con las filas y columnas pedidas. Investiga qué reglas definen las pistas de Grid. Trabaja en `.board`; cuando consigas el tablero, sigue la indicación del comentario sobre el borde naranja.

**Comprueba:** hay cinco casillas por fila, seis filas y ninguna casilla fuera del tablero.

### Parte 2: teclado con Flexbox

**Objetivo:** distribuir las teclas de `.keyboard` de forma que pasen a una nueva fila cuando falte espacio.

**Guía:** observa el ancho de las teclas y del teclado. Investiga cómo permitir varias filas en un contenedor flexible y cómo distribuir las teclas dentro de cada una. Cambia el ancho de la ventana para comprobar el resultado.

**Comprueba:** aparecen las 26 letras en orden, sin solaparse; en una ventana estrecha ocupan más filas que en una ancha.

<details>
<summary>Pistas para el tablero y el teclado</summary>

- Si el tablero no forma una matriz, revisa si `.board` es un contenedor Grid y si has definido filas y columnas.
- Si las teclas se salen del ancho disponible, revisa si el contenedor Flexbox permite una nueva fila.

</details>

## Recursos de consulta

- [Introducción a CSS Grid en MDN](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/CSS_layout/Grids): columnas, filas, `fr` y colocación.
- [Ejercicios de Grid en MDN](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/CSS_layout/Test_your_skills/Grid): actividades relacionadas con los cuatro primeros archivos.
- [Introducción a Flexbox en MDN](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/CSS_layout/Flexbox): distribución de elementos.
- [Consultas de medios en MDN](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/CSS_layout/Media_queries): cambio de diseño según el ancho de la ventana.
