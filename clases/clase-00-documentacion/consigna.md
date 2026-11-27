# Clase 0B — Entrada en Calor: Cómo Leer Documentación y Ser Autodidacta

## Objetivo
Aprender a **leer documentación oficial** (como MDN Web Docs) sin caer en copiar y pegar código a ciegas, incorporar el hábito autodidacta de investigar y probar propiedades hasta entenderlas, y reforzar el flujo profesional de **Fork + Pull Request** documentando con tus propias palabras lo que aprendiste.

---

## Cómo leer documentación sin marearte

La documentación técnica **no se lee como un libro** de principio a fin. Se usa como un mapa para encontrar rápido lo que necesitás y probarlo.

### Anatomía de una página en MDN (qué mirar en orden)
1. **Descripción inicial:** las primeras 2 o 3 líneas explican qué hace la etiqueta o propiedad.
2. **Ejemplo interactivo (*Try it*):** cambiale los valores ahí mismo para ver qué pasa en tiempo real.
3. **Sintaxis y valores:** qué opciones acepta (por ejemplo: `%`, `px`, `center`, `space-between`, `column`).
4. **Qué podés saltear al principio:** especificaciones técnicas (W3C) y tablas viejas de compatibilidad de navegadores.

### Cómo buscar bien en Google
Usá siempre la fórmula **`tecnología + qué querés lograr + mdn`**, por ejemplo:
- `css round corners mdn`
- `css box shadow mdn`
- `css flexbox align items mdn`

### La regla de oro: "Romper para entender"
Copiar un ejemplo solo sirve si después **le cambiás al menos 2 cosas** para ver qué cambia o por qué se rompe. Si no podés explicar qué hace cada línea con tus palabras, todavía no lo entendiste.

---

## Comandos básicos de terminal (CLI)

Antes de correr comandos de Git o de Node.js en Semana 1, te conviene dominar estos comandos mínimos en la terminal de VS Code (`Ctrl + ñ` o `` Ctrl + ` ``):

| Comando / Atajo | Qué hace |
| :--- | :--- |
| `pwd` | Muestra **dónde estás parado** (ruta completa de la carpeta actual). |
| `ls` | Lista los archivos y carpetas que hay en tu ubicación actual. |
| `cd <carpeta>` | Entra a esa carpeta (ej. `cd entregas`). |
| `cd ..` | Sube un nivel hacia la carpeta padre. |
| `mkdir <nombre>` | Crea una carpeta nueva. |
| `clear` | Limpia la pantalla de la terminal. |
| `Tab` | Autocompleta nombres de carpetas y archivos (evita errores de tipeo). |
| `↑` / `↓` | Recorre el historial de comandos que ya ejecutaste. |
| `Ctrl + C` | Cancela un proceso o comando que quedó corriendo. |

> **Error #1 más común:** correr `git status` o `node archivo.ts` estando parado en la carpeta equivocada. Antes de ejecutar un comando, verificá siempre con `pwd` y `ls` que estás dentro de `curso-repo`.

---

## Recursos Permitidos
- [MDN Web Docs — Referencia de CSS](https://developer.mozilla.org/es/docs/Web/CSS/Reference)
- [MDN Web Docs — Referencia de HTML](https://developer.mozilla.org/es/docs/Web/HTML/Element)
- [Markdown Guide — Sintaxis Básica](https://www.markdownguide.org/basic-syntax/) (para dar formato a tus apuntes)

---

## Consigna (Entregable: Tu Propia Documentación)

Creá dentro de `entregas/<tu-usuario-github>/clase-00-documentacion/` un archivo llamado **`apuntes.md`**.

Tu objetivo es **armar tu propia mini-documentación** con lo que investigaste leyendo **MDN** (y lo que practicaste en *Flexbox Froggy* y *CSS Diner*).

El archivo `apuntes.md` tiene que documentar **al menos 6 temas/propiedades**:
- **3 conceptos o propiedades que ya venimos usando** (por ejemplo: `width` en `%`, `display: flex`, `justify-content`, `align-items`, `flex-direction`, selectores descendientes como `a img` vs clases `.mi-clase`, `padding` vs `margin`).
- **3 propiedades nuevas de CSS o etiquetas HTML que NO vimos en clase** y tengas que buscar desde cero en MDN (ideas: `border-radius`, `box-shadow`, `opacity`, `cursor`, `:hover`, `gap`, `object-fit`, `transform`, `transition`, o las que elijas).

### Formato obligatorio para cada ficha
Para cada uno de los 6 temas, incluí:
1. **Nombre** de la propiedad o etiqueta.
2. **Enlace oficial a MDN** de donde lo leíste.
3. **Qué hace (con tus palabras):** explicado simple, como si se lo explicaras a un amigo.
4. **Valores principales:** al menos 2 o 3 valores que acepta y qué hace cada uno.
5. **Ejemplo propio:** un bloque de código (`css` o `html`) inventado por vos, **no copiado tal cual del ejemplo de MDN**.
6. **Qué probé / qué descubrí:** una frase contando qué cambiaste para comprobar que entendiste cómo funciona.

### Plantilla de ejemplo para tus fichas

````markdown
## 1. `border-radius`
- **Documentación oficial:** [MDN - border-radius](https://developer.mozilla.org/es/docs/Web/CSS/border-radius)
- **Qué hace:** Redondea las esquinas de una caja (un botón, una tarjeta o una imagen).
- **Valores principales:**
  - En `px` (ej. `8px`): esquinas apenas redondeadas.
  - En `%` (ej. `50%`): si el elemento es cuadrado, lo vuelve un círculo.
- **Ejemplo propio:**
```css
.avatar {
  width: 120px;
  height: 120px;
  border-radius: 50%;
}
```
- **Qué probé:** Si le pongo `50%` a un rectángulo que no es cuadrado, en vez de un círculo queda un óvalo.
````

> **Bonus (opcional):** Si querés probar lo que documentaste en el navegador, podés sumar un `index.html` y `styles.css` dentro de la misma carpeta `entregas/<tu-usuario-github>/clase-00-documentacion/`.

### Reglas de entrega
- **Prohibido copiar y pegar texto de MDN o respuestas generadas por IA.** En la revisión te vamos a preguntar por cualquiera de tus fichas y tenés que poder explicarla sin leer.
- Si consultaste alguna duda puntual con IA, declaralo con honestidad en la plantilla del PR.

---

## Cómo entregarla
1. Abrí la terminal en VS Code dentro de `curso-repo` (verificá con `pwd` y `ls`).
2. Actualizá tu fork (`Sync fork` en GitHub + `git checkout main` y `git pull origin main` en tu PC).
3. Creá la rama `entrega/clase-00-documentacion` y tu carpeta desde la terminal:
   ```bash
   git checkout -b entrega/clase-00-documentacion
   mkdir entregas/<tu-usuario-github>/clase-00-documentacion
   ```
4. Trabajá **únicamente** dentro de `entregas/<tu-usuario-github>/clase-00-documentacion/`.
5. Guardá y subí tus cambios:
   ```bash
   git add .
   git commit -m "docs: apuntes de lectura de documentacion"
   git push origin entrega/clase-00-documentacion
   ```
6. Abrí el Pull Request siguiendo [`docs/flujo-entregas.md`](../../docs/flujo-entregas.md) y verificá que el check automático **`evaluar-pr`** quede en verde.
