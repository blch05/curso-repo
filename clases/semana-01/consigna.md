# Semana 1 — TypeScript: Variables, Tipos Primitivos, Condicionales y Bucles

## Objetivo
Dar los primeros pasos en **TypeScript moderno** ejecutado nativamente con Node.js LTS (`node archivo.ts`), dominar variables, tipos primitivos explícitos, condicionales (`if/else`) y bucles (`for`, `while`), y afianzar el flujo de trabajo con **Git, Terminal y Pull Requests**.

## Diccionario de la Industria
- Código fuente y terminal/consola
- TypeScript vs. JavaScript (tipado estático, transpilación y *type stripping* en Node.js vs. chequeo de tipos en VS Code)
- **Scope** (alcance de variables en bloques `{ }`) y **`null` vs. `undefined`**
- Control de versiones (`Git` vs. `GitHub`), repositorio, rama (*branch*), commit, Fork y Pull Request

## Recursos Permitidos
- [es.javascript.info — Fundamentos de JavaScript](https://es.javascript.info/first-steps)
- [TypeScript Handbook — Everyday Types](https://www.typescriptlang.org/docs/handbook/2/everyday-types.html)

## Reglas Técnicas de esta Semana
- **Tipos explícitos siempre** (`string`, `number`, `boolean` o *union literal* como `'+' | '-' | '*' | '/'`) y **cero `any`**.
- **Usar `const` por defecto** y `let` solo cuando el valor cambie (prohibido `var`). Usar siempre `===` / `!==`.
- **Solo lógica secuencial:** esta semana **NO se usan funciones, *arrow functions* ni arrays** (eso arranca en Semana 2).
- **Datos de entrada:** definí los valores de prueba como constantes tipadas al inicio de cada archivo (ej. `const numero: number = 7;`). Para probar otros casos, cambiá el valor, guardá (`Ctrl + S`) y volvé a ejecutar.
- **Cero errores en VS Code:** Node.js LTS ejecuta `.ts` borrando los tipos al vuelo (*type stripping*), por lo que **no frena errores de tipos al correr**. Antes de hacer commit, verificá que VS Code no muestre ningún subrayado rojo.

### Cómo ejecutar tus ejercicios desde la terminal
Parate dentro de tu carpeta de entrega y corré cada archivo con `node`:
```bash
cd entregas/<tu-usuario-github>/semana-01
node 01-presentacion.ts
```
*(Tip: usá `Tab` para autocompletar nombres de archivos, `↑` para repetir el último comando y `Ctrl + C` si algún bucle `while` se queda colgado en un bucle infinito).*

## Consigna (Entregable 1)
Creá dentro de `entregas/<tu-usuario-github>/semana-01/` los siguientes **12 ejercicios cortos** en archivos `.ts`:

1. `01-presentacion.ts` — Declarar variables tipadas (`nombre`, `edad`, `ciudad`, `esEstudiante`) e imprimir una presentación formateada usando *template strings* (`` `...` ``).
2. `02-calculadora-basica.ts` — Dados dos números y un operador tipado con *union literal* (`'+' | '-' | '*' | '/'`), calcular y mostrar el resultado controlando división por cero.
3. `03-par-o-impar.ts` — Determinar si un número entero es par o impar (usando `%`) y si es positivo, negativo o cero.
4. `04-mayor-de-tres.ts` — Dados tres números, determinar cuál es el mayor usando condicionales (**sin usar `Math.max`**).
5. `05-descuento-comercio.ts` — Dado el monto de una compra y si el cliente es socio (`boolean`), aplicar 15 % de descuento si supera \$20.000 o 20 % si supera \$20.000 **y además** es socio. Mostrar el descuento aplicado y el total final.
6. `06-validador-nota.ts` — Dada una nota del 1 al 10, mostrar `"Desaprobado"` (< 7), `"Aprobado"` (7–8) o `"Excelente"` (9–10), validando primero que la nota esté dentro del rango 1–10.
7. `07-tabla-multiplicar.ts` — Imprimir la tabla de multiplicar del 1 al 10 de un número usando un bucle `for`.
8. `08-sumatoria-pares.ts` — Calcular la suma de todos los números pares entre 1 y `N` usando `for` y una variable acumuladora.
9. `09-cuenta-regresiva.ts` — Hacer una cuenta regresiva desde `N` hasta `0` usando `while` y finalizar imprimiendo `"¡Despegue!"`.
10. `10-factorial.ts` — Calcular el factorial de un número entero no negativo usando un bucle (recordar que `0! = 1` y validar si el número es negativo).
11. `11-fizzbuzz.ts` — Imprimir del 1 al 50: `"Fizz"` si es múltiplo de 3, `"Buzz"` si es múltiplo de 5, `"FizzBuzz"` si es múltiplo de ambos, o el número en caso contrario.
12. `12-piedra-papel-tijera.ts` — Simular 3 rondas entre jugador y computadora usando un bucle `for` (sin leer teclado; podés generar jugadas aleatorias con `Math.random()` o simular jugadas distintas por ronda), imprimir el resultado de cada ronda y mostrar el ganador final (o empate).

> **Nota sobre Git:** Subí tus avances en **al menos 3 commits separados** con mensajes descriptivos. Sugerencia:
> - Commit 1: `feat: ejercicios 1 a 4 semana 1`
> - Commit 2: `feat: ejercicios 5 a 8 semana 1`
> - Commit 3: `feat: ejercicios 9 a 12 semana 1`

## Cómo entregarla
1. Actualizá tu fork (`Sync fork` en GitHub + `git checkout main` + `git pull origin main`).
2. Creá la rama `entrega/semana-01` (`git checkout -b entrega/semana-01`).
3. Trabajá solo en `entregas/<tu-usuario-github>/semana-01/`.
4. Abrí el Pull Request antes del **jueves a las 23:59** siguiendo [`docs/flujo-entregas.md`](../../docs/flujo-entregas.md), completando la declaración de uso de IA y verificando que **`evaluar-pr` quede en verde**.
