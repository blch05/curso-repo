# Semana 10 — Backend Propio Seguro (Node.js + Express + TypeScript + JWT)

## Objetivo
Construir un servidor backend propio en **Node.js + Express con TypeScript**, configurando CORS y un middleware de autenticación que valide el `Authorization: Bearer <token>` enviado desde React antes de ejecutar lógica crítica de negocio, y probar/documentar los endpoints de forma aislada con **Postman**.

## Diccionario de la Industria
- Backend propio (cuándo y por qué hace falta: secretos, reglas críticas — **"nunca confiar en el cliente"**)
- Validación de límites en servidor y **Rate Limiting** (`HTTP 429`)
- Endpoint, Routing, Middleware, CORS
- `Authorization: Bearer <token>` y validación de JWT
- Pruebas aisladas de API con **Postman** y contrato de API (**OpenAPI / Swagger**)

## Recursos Permitidos
- [Express Docs — Routing y Middleware](https://expressjs.com/es/guide/routing.html)
- [Postman Learning Center](https://learning.postman.com/)
- [Swagger / OpenAPI Docs](https://swagger.io/docs)

## Consigna (Entregable 10)
Dentro de `entregas/<tu-usuario-github>/mvp/backend/` (o carpeta `server/`):

1. Inicializá un servidor Express con TypeScript (`express`, `cors`, `@supabase/supabase-js`, `@types/express`, `@types/cors`).
2. Creá un **middleware de autenticación** que lea el header `Authorization: Bearer <token>` y verifique el usuario con `supabase.auth.getUser(token)` (devolviendo `401` si falta o es inválido, y `403` si el rol no corresponde).
3. Implementá al menos **1 o 2 endpoints propios** para reglas críticas de tu MVP (ej. validación antisolapamiento de turnos, cálculo de vencimientos, descuento atómico de stock o cierre de caja diario).
4. **Pruebas y documentación de tu API (obligatorio antes de conectar React):**
   - Probá cada endpoint en **Postman** cubriendo los casos clave: sin token (`401`), rol incorrecto si aplica (`403`), payload inválido (`400`) y petición válida con `Authorization: Bearer <token>` (`200`/`201`).
   - Exportá la colección de Postman como `postman_collection.json` dentro de la carpeta del backend **sin tokens ni secretos hardcodeados** (usá variables como `{{BASE_URL}}` y `{{TOKEN}}`).
   - Agregá en el `README.md` del backend una tabla breve con el contrato de cada endpoint (método, ruta, headers requeridos, ejemplo de body JSON y códigos de respuesta).
   - *(Bonus opcional)* Exponer `/api-docs` con `swagger-ui-express` + un archivo `openapi.yaml` describiendo tus endpoints propios.
5. Consumí esos endpoints desde tu frontend React enviando el token de la sesión activa.

## Cómo entregarla
Seguí [`docs/flujo-entregas.md`](../../docs/flujo-entregas.md) en la rama `entrega/semana-10` antes del **jueves a las 23:59**.
