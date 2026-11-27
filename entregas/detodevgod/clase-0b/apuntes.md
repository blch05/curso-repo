## 1. `padding`
- **Documentación oficial:** [MDN-padding](https://developer.mozilla.org/es/docs/Web/CSS/Reference/Properties/padding)
- **Qué hace:** establece el área de relleno en los cuatro lados de un elemento a la vez.
- **Valores principales:**
  - En `px` (ej. `8px`): El tamaño del relleno como un valor fijo.
  - En `%` (ej. `50%` de 400 px si el contenedor mide eso nos da un 200px de pading): El tamaño del relleno como porcentaje tomando en cuenta como referencia el ancho del elemento contenedor
- **Ejemplo propio:**
```css
.contenedor {
    padding: 100px;
}
.caja{
    Padding: 10%px 
}
```
- **Qué probé:** Si le pongo `10%`y el contenedor mide 100px , se aplicara un padding de 10% a cada lado (10px)

## 2. `Background image`
- **Documentación oficial:** [MDN - Background image](https://developer.mozilla.org/es/docs/Web/CSS/Reference/Properties/background-image)
- **Qué hace:** Agrega una imagen el fondo de tu pagina web, se puede hacer resizing o cambiar parametros con otros comandos relacionados al background pero no los probe.
- **Valores principales:**
  -background-image: url("/shared-assets/images/examples/lizard.png");
- **Ejemplo propio:**
```css
body {
 background-image: url("https://preview.redd.it/i-spent-the-last-9-hours-building-this-huge-magical-library-v0-j760zttlgjj71.png?width=1080&crop=smart&auto=webp&s=9ae0697e1b78d99f1b565a154c11144bc28a3952");
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
    background-attachment: fixed;
}
```
- **Qué probé:** Le puse una imagen de fondo y use los parametros para q cubra toda la pag, que este ubicado en el centro y q no se repita cdo llegue al fin de la img.
## 3. `Display`
- **Documentación oficial:** [MDN - display](https://developer.mozilla.org/en-US/docs/Web/CSS/Guides/Display)
- **Qué hace:** El módulo CSS display define cómo se muestra un elemento en la página y cómo se comporta respecto a los demás elementos.
- **Valores principales:**
  - En block ocupa todo el ancho disponible y comienza una linea nueva
  - En flex organiza los elementos en fila
  - En inline ocupa solo el espacio de su contenido y puede compartir línea con otros elementos.
- **Ejemplo propio:**
```css
.contenedor {
 display: flex;
 flex-direction: column;
}
```
- **Qué probé:** Si le pongo display flex, teniendo qsy un h1 y un p en mi html me los pondra al lado del otro, pero como le pongo column el h1 se va a poner arriba del p

<h1>AHORA LAS Q NO USE NUNCA</h1>


## 4. `Text Shadow`
- **Documentación oficial:** [MDN - text decoration-text shadow](https://developer.mozilla.org/en-US/docs/Web/CSS/Guides/Text_decoration/Text_shadows)
- **Qué hace:** es una decoracion para ponerle sombra a un texto, cada sombra precisa minimo 2 valores de lenght, hasta 3 creo con los cuales controlas el desplazamiento horizontal, el desplazamiento vertical, el desenfoque y tmb se le puede poner un valor de color.
- **Valores principales:**
    Primer valor: desplazamiento horizontal (x).
    Segundo valor: desplazamiento vertical (y).
    Tercer valor (opcional): radio de desenfoque (blur).
    Cuarto valor (opcional): color de la sombra.
- **Ejemplo propio:**
```css
.titilo {
  text-shadow: 2px 2px 4px gray
}
```
- **Qué probé:** Si aumento los valores horizontales y verticales, la sombra se aleja más del texto. Si aumento el valor de desenfoque (blur), la sombra se ve más suave y difusa. y el color es de la bombacha de cristian 
## 5. `span`
- **Documentación oficial:** [MDN - span](https://developer.mozilla.org/es/docs/Web/HTML/Reference/Elements/span)
- **Qué hace:** El elemento <span> se utiliza para agrupar o marcar una parte de texto sin agregar ningún significado especial. Se usa principalmente para aplicar estilos o manipular una porción específica del contenido con CSS. a diferencia de div agrupa texto en linea no en bloque
- **Valores principales:**
  - <span></span>
- **Ejemplo propio:**
`<div style="border: 1px dotted blue;">
  <h4>soyy rrregayyyyy</h4>
  <p>
    Esto es un párrafo dentro de un div,
    <span style="color: red;"> y esto un span dentro de un párrafo. </span>
  </p>
</div>

```
- **Qué probé:** basicamente span es una division mas chica q div, div selecciona todo el bloque y spann una parte de este o linea, y ahi le pongo un color azul a todo el borde del bloque con div y color rojo a la parte de span.

## 6. `time`
- **Documentación oficial:** [MDN - time](https://developer.mozilla.org/es/docs/Web/HTML/Reference/Elements/time)
- **Qué hace:** El elemento HTML <time> representa un periodo específico en el tiempo. Puede incluir el atributo datetime para convertir las fechas en un formato interno legible por un ordenador, permitiendo mejores resultados en los motores de búsqueda o características personalizadas como poner una hora del fin de una oferta qsy.
- **Valores principales:**
  - datetime: especifica la fecha u hora en un formato legible para máquinas.
  - Contenido del elemento: la fecha u hora que verá el usuario.
- **Ejemplo propio:**
```html
<p>La entrega es el <time datetime="2026-11-30">30 de noviembre de 2026</time>.</p>
```
- **Qué probé:** Mostré una fecha usando <time> y agregué el atributo datetime. La fecha se ve normal para el usuario, pero el navegador puede reconocer que representa una fecha específica.