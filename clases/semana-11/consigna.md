# Semana 11 — Emancipación del MVP, Deploy a Producción, Dominios y DNS

## Objetivo
Congelar el alcance del **MVP (*Minimum Viable Product*)**, emancipar tu proyecto a **tu propio repositorio independiente** en GitHub, desplegar Frontend (Vercel) y Backend Express (Render) en internet y comprender cómo conectar un dominio propio mediante DNS y HTTPS/SSL.

## Diccionario de la Industria
- `MVP` (*Minimum Viable Product*)
- `Deploy` y entornos (`localhost` vs. `production`)
- Variables de entorno en la nube y logs de producción
- Dominio, DNS (`A` / `CNAME`) y certificados HTTPS/SSL

## Consigna (Entregable 11)
1. **Emancipación del MVP:** Extraé `entregas/<tu-usuario-github>/mvp/` a un **repositorio nuevo e independiente** en tu cuenta personal de GitHub con un `README.md` claro (descripción, capturas, stack, cómo correrlo y la **documentación de tus endpoints propios** + `postman_collection.json`, o link a `/api-docs` si hiciste el bonus de Swagger).
2. **Deploy en Producción:**
   - Desplegá el Backend Express en **Render** con sus variables de entorno y CORS apuntando a tu frontend, y verificá los endpoints en producción con **Postman**.
   - Desplegá el Frontend React en **Vercel** con `VITE_SUPABASE_URL`, `VITE_SUPABASE_ANON_KEY` y la URL de tu backend en Render.
3. **Registro en el Campus:** Compartí el título de tu sistema, tu URL pública en Vercel y el enlace a tu nuevo repositorio independiente para darlo de alta en la galería privada del Campus (Supabase).

## Cómo entregarla
Verificá que tu app desplegada funcione de punta a punta desde celular y PC antes del **jueves a las 23:59** y enviá los links de producción + repositorio al canal de entregas.
