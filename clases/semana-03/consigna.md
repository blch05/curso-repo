# Semana 3 — Arquitectura Web, HTTP, APIs REST y Asincronía

## Objetivo
Comprender cómo se comunican Cliente y Servidor mediante HTTP, probar endpoints en **Postman**, leer documentación básica **OpenAPI / Swagger**, consumir APIs REST reales usando `fetch()`, `async / await` y `try / catch` con respuestas tipadas en TypeScript, e inspeccionar peticiones en la pestaña **Network** de DevTools.

## Diccionario de la Industria
- **DOM (*Document Object Model*)**, árbol de nodos, eventos del navegador y DevTools (*Elements* + *Network*)
- **Single-thread y Event Loop** conceptual (por qué existe la asincronía para no congelar la interfaz)
- Frontend (Cliente) vs. Backend (Servidor)
- Protocolo HTTP (*Request/Response*, verbos `GET`/`POST`, headers, status codes `200`, `400`, `401`, `404`, `500`)
- API y API REST
- Cliente HTTP (**Postman**) y lectura básica de documentación **OpenAPI / Swagger**
- Promesas (`Promise<T>`), `async / await`, `try / catch`

## Recursos Permitidos
- [es.javascript.info — Async/await](https://es.javascript.info/async-await)
- [es.javascript.info — Fetch](https://es.javascript.info/fetch)
- [MDN — Códigos de estado HTTP](https://developer.mozilla.org/es/docs/Web/HTTP/Status)
- [Postman Learning Center](https://learning.postman.com/)
- [Swagger / OpenAPI Docs](https://swagger.io/docs)

## Consigna (Entregable 3)
Trabajá dentro de `entregas/<tu-usuario-github>/semana-03/`:

1. **Exploración previa en Postman:** Antes de escribir código, probá en **Postman** al menos 2 peticiones `GET` contra la API pública elegida (ej. Rick & Morty API o PokéAPI): una consulta válida (`200 OK`) y un recurso inexistente (`404 Not Found`) para inspeccionar headers, status code y la estructura real del JSON que vas a tipar.
2. **Parte 1 (Consola Node.js):** Creá `api-consola.ts` que consuma esa API pública, tipe la respuesta con `interface` según lo observado en Postman, maneje errores con `try / catch` y valide `response.ok`.
3. **Parte 2 (Esqueleto Web con Vite `vanilla-ts`):** Completá el código TypeScript para:
   - Consultar la API pública al cargar y al buscar/filtrar.
   - Mostrar estado de carga (`"Cargando..."`) mientras se resuelve la promesa.
   - Mostrar un mensaje de error claro si falla la red o devuelve `404`/`500`.
   - Renderizar los resultados filtrados en pantalla.

## Cómo entregarla
Seguí los 5 pasos de [`docs/flujo-entregas.md`](../../docs/flujo-entregas.md) en la rama `entrega/semana-03` antes del **jueves a las 23:59**.
