# Diccionario Obligatorio de la Industria

Conceptos que debés poder explicar con tus propias palabras en los exámenes orales:

## Web, Navegador y Red
- **Frontend (Cliente):** Código que corre en el navegador del usuario (React, HTML, CSS, TS).
- **Backend (Servidor):** Código que corre en un servidor privado, valida reglas de negocio, habla con la base de datos y protege secretos.
- **DOM (*Document Object Model*):** Representación en árbol de nodos que construye el navegador a partir del HTML para renderizar la página y escuchar eventos del usuario.
- **HTML Semántico, Box Model y Responsive:** Uso de etiquetas con significado (`<header>`, `<main>`, `<nav>`, `<button>`), modelo de caja CSS (`margin`, `border`, `padding`, `content`) y diseño adaptable a celular y PC (*mobile-first*).
- **Single-thread y Event Loop (conceptual):** JavaScript ejecuta una tarea principal a la vez; la asincronía (`Promise` / `async-await`) delega operaciones lentas (como `fetch`) para no congelar la interfaz.
- **HTTP:** Protocolo de comunicación Request/Response entre cliente y servidor. Verbos principales: `GET`, `POST`, `PUT`/`PATCH`, `DELETE`. Códigos clave: `200` (OK), `201` (Created), `400` (Bad Request), `401` (Unauthorized), `403` (Forbidden), `404` (Not Found), `429` (Too Many Requests), `500` (Server Error).
- **API / API REST:** Interfaz de endpoints HTTP que intercambian datos (generalmente en JSON) siguiendo convenciones estándar.
- **Cliente HTTP (Postman):** Herramienta estándar de la industria para enviar peticiones HTTP (`GET`, `POST`, `PUT`/`PATCH`, `DELETE`) con headers y body JSON, inspeccionar respuestas y probar endpoints de forma aislada antes de conectar el frontend.
- **OpenAPI / Swagger:** Estándar oficial (**OpenAPI**) para describir el contrato de una API REST (rutas, parámetros, headers, payloads y códigos de respuesta) y conjunto de herramientas (**Swagger UI**) que generan documentación interactiva (*Try it out*).
- **CORS:** Mecanismo de seguridad del navegador que controla qué dominios tienen permiso para consultar un backend.
- **Dominio, DNS (`A` / `CNAME`) y HTTPS/SSL:** El nombre legible de un sitio (`negocio.com.ar`), el sistema que traduce ese nombre a la IP/servidor real, y el cifrado seguro de la conexión.

## Programación, Datos y React Moderno
- **TypeScript vs. JavaScript:** TypeScript agrega tipado estático a JavaScript para detectar errores antes de ejecutar el código; al final se transpila a JS para el navegador.
- **Scope y `null` vs. `undefined`:** Alcance donde existe una variable (bloque/función); `undefined` significa "no asignado", mientras que `null` representa "vacío intencional".
- **Paso por valor vs. por referencia:** Los primitivos (`number`, `string`, `boolean`) se copian por valor; los objetos y arrays se pasan por referencia (asignar `const b = a` apunta al mismo objeto en memoria, por eso en React usamos inmutabilidad).
- **JSON:** Formato de texto estándar para intercambiar datos estructurados entre sistemas.
- **CRUD:** Las 4 operaciones básicas sobre datos: *Create, Read, Update, Delete*.
- **SQL vs. NoSQL:** Bases de datos relacionales (tablas con esquemas, `PK`, `FK`, `JOIN`, como PostgreSQL) vs. no relacionales (documentos, clave-valor).
- **Arquitectura y Modelado Relacional (DER / Normalización):** Diseño previo de entidades, cardinalidad (`1:N`, `N:M` con tabla intermedia), normalización básica para evitar datos duplicados, restricciones (`NOT NULL`, `UNIQUE`, `CHECK`) e índices.
- **DOM imperativo vs. React declarativo:** En vez de manipular nodos a mano (`querySelector`), en React describís la UI en función del estado (`UI = f(state)`).
- **Los 4 estados de toda UI:** Toda pantalla conectada a datos remotos debe manejar **Loading** (skeleton/spinner), **Empty** (sin datos), **Error** (mensaje claro) y **Data**.
- **Custom Hooks:** Funciones `use...` en React para encapsular y reutilizar lógica de estado o consumo de datos.
- **Server State vs. Client Global State:** Datos remotos cacheados y sincronizados con el servidor (**TanStack Query**) vs. estado global local del navegador (**Zustand**; alternativa histórica: **Redux**).

## Seguridad
- **Autenticación vs. Autorización:** Autenticación = *quién sos* (Login / JWT). Autorización = *qué tenés permiso de hacer* (Roles `admin`/`usuario`, políticas **RLS**).
- **`localStorage` / `sessionStorage` vs. `Cookies` (`HttpOnly`):** Almacenamiento en el navegador; las cookies `HttpOnly` no pueden ser leídas por JavaScript (mitigan XSS), mientras que `localStorage` sí es accesible desde JS.
- **SQL Injection:** Vulnerabilidad al concatenar texto del usuario dentro de una consulta SQL; se previene usando consultas parametrizadas / SDK.
- **Nunca confiar en el cliente + Rate Limiting:** Toda regla crítica y límite de campos se valida siempre en el servidor/BD, y el *Rate Limiting* frena ataques de fuerza bruta o abuso de endpoints (`HTTP 429`).
- **Variables de entorno (`.env`):** Claves y configuraciones sensibles que viven fuera del código y jamás se suben a GitHub (`.gitignore`).

## Producto y Flujo de Trabajo
- **MVP (*Minimum Viable Product*):** Versión mínima funcional y vendible de un producto real.
- **Deploy:** Publicar la aplicación en servidores de producción (`localhost` -> internet).
- **Git, GitHub, Fork y Pull Request:** Control de versiones distribuido y flujo profesional de revisión de código.
