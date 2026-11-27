
# CLASE 00 - Consigna B

## 1. `color`
- **Documentación oficial:** [MDN - color](https://developer.mozilla.org/es/docs/Web/CSS/Reference/Properties/color)
- **Qué hace:** define el color del texto de la etiqueta seleccionada.
- **Valores principales:**
    - Colores predefinidos (Ej: `red`): define el color del texto en rojo.
    - Valores en Hexadecimal (Ej: `#48e`): permite definir un color más personalizado (azul claro, en este caso).
- **Ejemplo propio**
```css
h3 {
    font-family: 'Inter';
    font-size: 16px;
    color: #48e;
}
```
- **Qué probé:** empecé a cambiar cada valor para entender cómo cambiaban los tonos y qué color representa cada dígito. 

## 2. `cursor`
- **Documentación oficial:** [MDN - cursor](https://developer.mozilla.org/es/docs/Web/CSS/Reference/Properties/cursor)
- **Qué hace:** define el estilo del cursor o mouse al pasarlo por cierto elemento de la página.
- **Valores principales:**
    - Cursores de links y estados (Ej: `pointer`): al pasar por un elemento, pone el cursor de la manito.
    - Cursores de selección (Ej: `text`): pone el cursor de la línea vertical, de cuando seleccionas texto.
- **Ejemplo propio**
```css
.button-submit {
    padding: 10px 15px;
    background-color: #48e;
    cursor: pointer;
}
```
- **Qué probé:** probé aplicar distintos tipos de cursores y ver qué se mostraba al pasar el mouse por un botón.

## 3. `font-size`
- **Documentación oficial:** [MDN - font-size](https://developer.mozilla.org/es/docs/Web/CSS/Reference/Properties/font-size)
- **Qué hace:** establece el tamaño del texto.
- **Valores principales:**
    - En píxeles (Ej: `16px`): define el tamaño de la fuente en 16px.
    - En rem (length) (Ej: `1rem`): define el tamaño de la fuente en un 1rem (equivalente a 16px)
- **Ejemplo propio**
```css
ul li {
    font-family: 'sans-serif';
    font-size: 1rem;
    color: #222;
}
```
- **Qué probé:** comparé el cambio de tamaño de la fuente pasando de pixeles a rem.

## 4. `opacity`
- **Documentación oficial:** [MDN - opacity](https://developer.mozilla.org/es/docs/Web/CSS/Reference/Properties/opacity)
- **Qué hace:** maneja la opacidad de un elemento, su transparencia.
- **Valores principales:**
    - 0 <= x <= 1 (Ej: `0.5`): define la opacidad del elemento a la mitad (50% opaco).
- **Ejemplo propio**
```css
.div-filtro {
    height: 270px;
    width: 270px;
    background-color: #bbb;
    opacity: 0.6;
}
```
- **Qué probé:** probé cambiando el valor de la opacidad para probar la distinta visiblidad que ofrecía.

## 5. `:empty`
- **Documentación oficial:** [MDN - :empty](https://developer.mozilla.org/es/docs/Web/CSS/Reference/Selectors/:empty)
- **Qué hace:** es una pseudoclase que selecciona todos los elementos sin hijos (se considera hijos a etiquetas, texto o un espacio en blanco).
- **Valores principales:**
    - Fondo distinto (Ej: `background-color: #283`): aplica un background verde a los elementos sin hijos.
    - Visibildiad (Ej: `display: none`): no muestra los elementos que no tengan hijos.
- **Ejemplo propio**
```css
div:empty {
    display: none;
}
```
- **Qué probé:** probé aplicar distintas propiedades como background-color y display para ver cómo interactuaba la etiqueta.

## 6. `:invalid`
- **Documentación oficial:** [MDN - :invalid](https://developer.mozilla.org/es/docs/Web/CSS/Reference/Selectors/:invalid)
- **Qué hace:** es una pseudoclase que selecciona los input y forms inválidos.
- **Valores principales:**
    - Borde remarcado (Ej: `border-color: #d22`): remarca con bordes rojos los inputs y forms inválidos.
    - Background resaltado (Ej: `background-color: #f77`): define un fondo rojo claro para los inputs y forms inválidos.
- **Ejemplo propio**
```css
input:invalid {
    background-color: #f77;
    color: #f22;
    border-color: #f22
}
```
- **Qué probé:** aplicar distintas propiedades para resaltar la invalidez de los campos.

