## 1. `margin-bottom`
- **Documentación oficial:** [MDN - margin-bottom](https://developer.mozilla.org/es/docs/Web/CSS/Reference/Properties/margin-bottom)
- **Qué hace:** es la propiedad de un elemento que establece el espacio requerido en la parte inferior de un elemento. Tambien se permiten valores negativos.
- **Valores principales:**
  - <length> Especifica un ancho fijo. Consulte los valores posibles.
  - <percentage> es relativo al ancho del bloque contenedor.
  - <auto> Ver margin.
- **Ejemplo propio:**
```css establece la distancia es un objeto que lo separa de la parte inferior de la caja 
.avatar {
  width: 120px;
  height: 120px;
  border-radius: 50%;
  margin-bottom: 16px;
}
```
- **Qué probé:** probe cambiando los pixeles de mi .foto de 16px a 100px lo cual alejaba la imagen del texto que contenia debajo 

## 2. `box-shadow`
- **Documentación oficial:** [MDN - box-shadow](https://developer.mozilla.org/es/docs/Web/CSS/Reference/Properties/box-shadow)
- **Qué hace:** añade efectos de sombra alrededor del marco de un elemento. Se pueden definir múltiples efectos separados por comas. La caja de la sombra se describe por los desplazamientos en X e Y, los radios de desenfoque y dispersión, y el color relativos al elemento.
- **Valores principales:**
  - <offset-x> <offset-y> para definir el desplazamiento de la sombra
  - <blur-radius> Cuando mayor sea este valor, mayor sera la difuminación, por consecuencia la sombra se vuelve más grande y ligera.
  - <inset> La presencia de la palabra clave inset cambia la sombra a una dentro del marco (como si el contenido estuviera deprimido dentro de la caja)

- **Ejemplo propio:** crea diferentes formas y sombra dentro y fuera de la caja las cuales podes ir modificando con una serie de subcomandos
```css
blockquote {
  padding: 20px;
  box-shadow:
    inset 0 -3em 3em rgba(0, 0, 0, 0.1),
    0 0 0 2px rgb(255, 255, 255),
    0.3em 0.3em 1em rgba(0, 0, 0, 0.3);
}
}
```
- **Qué probé:** utilize el comando inset lo cual invirtio el valor de la sombra dentro del marco 

## 3. `ul`
- **Documentación oficial:** [MDN - ul](https://developer.mozilla.org/es/docs/Web/HTML/Reference/Elements/ul)
- **Qué hace:** crea una lista no ordenada.
- **Valores principales:**
  - Sus etiquetas son: <ul> y </ul> (ambas obligatorias).
- **Ejemplo propio:** crea una lista desordenada de items
```html
<ul>
 <li>Esto</li>
 <li>Lo otro</li>
 <li>Lo de más allá</li>
</ul>
```
- **Qué probé:** cree una lista de items

## 4. `<video>`
- **Documentación oficial:** [MDN - <video>](https://developer.mozilla.org/es/docs/Web/HTML/Reference/Elements/video)
- **Qué hace:** incrusta en el documento un reproductor multimedia compatible con la reproducción de vídeo. También puedes usar <video> para contenido de audio.
- **Valores principales:**
  - <source> el navegador intenta cargar cada fuente de forma secuencial. Si una fuente falla (por ejemplo, debido a una URL no válida o a un formato no admitido), se intenta con la siguiente, y así sucesivamente
  - <loop> el navegador volverá automáticamente al inicio al llegar al final del vídeo.
- **Ejemplo propio:**reproduce un video sobre el formato ya creado
```html
<video controls>
  <source src="myVideo.webm" type="video/webm" />
  <source src="myVideo.mp4" type="video/mp4" />
  <p>
    <a href="myVideo.mp4" download="myVideo.mp4">enlace al vídeo</a>.
  </p>
</video>
```
- **Qué probé:** probe colocando un video sobre mi tarjeta de presentacion

## 5. `<iframe>`
- **Documentación oficial:** [MDN - <iframe>](https://developer.mozilla.org/es/docs/Web/HTML/Reference/Elements/iframe)
- **Qué hace:** representa un contexto de navegación añadido, el cual permite incrustrar otra página HTML en la página actual.
- **Valores principales:**
  - <sandbox> Aplica restricciones adicionales al contenido del marco. El valor del atributo puede estar vacío para aplicar todas las restricciones, o bien contener tokens separados por espacios para eliminar restricciones específicas.
  - <allow-modals>Permite que el recurso abra ventanas modales.
- **Ejemplo propio:**
```html
<iframe
  id="inlineFrameExample"
  title="Inline Frame Example"
  width="300"
  height="200"
  src="https://www.openstreetmap.org/export/embed.html?bbox=-0.004017949104309083%2C51.47612752641776%2C0.00030577182769775396%2C51.478569861898606am;layer=mapnik">
</iframe>

- **Qué probé:** me permitio colocar un video directo de you tube sin descargarlo directamente de la url.

## 6. `justify-content`
- **Documentación oficial:** [MDN - justify-content](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Properties/justify-content)
- **Qué hace:** define cómo el navegador distribuye el espacio entre y alrededor de los items flex, a lo largo del eje principal de su contenedor.
- **Valores principales:**
  - flex-start Los items flex se colocan comenzando desde el comienzo principal. El margen del primer item es alineado al ras con el borde del comienzo principal de la línea y cada item siguiente es alineado al ras con el precedente.
  - flex-end Los items flex se colocan comenzando desde el final principal. El margen del último item es alineado al ras con el borde del final principal de la línea y cada item precedente es alineado al ras con el siguiente.
- **Ejemplo propio:** determina el movimiento de los items por el espacio y los da un limite    
```css
/* Alinear items flex desde el comienzo */
justify-content: flex-start;

/* Alinear items desde el final */
justify-content: flex-end;

/* Alinear items en el centro */
justify-content: center;

/* Distribuir items uniformemente
El primer item al inicio, el último al final */
justify-content: space-between;

```
- **Qué probé:** utilice justify-content: center y llevo todos los items al centro
