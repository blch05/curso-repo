# Programa Oficial — Bootcamp de Programación Web desde Cero (v2)

**Duración estimada:** 12 semanas  
**Grupo:** Cohorte reducida (1 a 3 personas)  
**Modalidad:** Encuentros en vivo los fines de semana (2 a 4 hs semanales, viernes y/o sábado) + práctica autónoma obligatoria durante la semana (6 a 8 hs).  
**Nivel inicial requerido:** Ninguno (desde cero absoluto).

---

## 1. Objetivo del Curso

Que al finalizar las 12 semanas seas capaz de **pensar, programar, conectar a una base de datos y desplegar en internet un proyecto web propio**, entendiendo qué ocurre por debajo en cada capa y manejando el vocabulario técnico real de la industria.

Este curso no entrega un título ni certificado formal: el objetivo real es que termines con bases sólidas, criterio técnico y **un producto web propio, publicado en tu cuenta de GitHub, listo para mostrar en tu portfolio o vender a un cliente real**.

---

## 2. Stack Tecnológico que Vas a Aprender

- **Lenguaje:** TypeScript moderno (ejecutado nativamente en Node.js LTS, estándar actual de la industria).
- **Frontend:** React + Vite + Tailwind CSS + **Custom Hooks**, **TanStack Query** (estado del servidor) y **Zustand** (estado global de cliente).
- **Base de Datos y Autenticación:** Supabase (PostgreSQL con SQL escrito a mano + roles + políticas de seguridad RLS).
- **Backend Propio y APIs:** Node.js + Express en TypeScript (con validación de JWT y roles), **Postman** (pruebas aisladas y colecciones) y lectura de contratos **OpenAPI / Swagger**.
- **Flujo de Trabajo y Producción:** Git, GitHub (flujo profesional de Fork + Pull Requests), Vercel y Render.

---

## 3. Cómo Funcionan las Clases y las Entregas

### Clase 0 — Entrada en Calor (Pre-trabajo obligatorio antes de la Clase 1)
Para aprovechar el tiempo de clase programando y no instalando programas, debés llegar a la Clase 1 con **VS Code, Node.js (LTS), Git, las extensiones recomendadas, tu cuenta de GitHub, el Fork del repositorio del curso** y tu **primer Pull Request abierto** (la tarjeta de presentación en HTML + CSS de `clases/clase-00/consigna.md`). Al inicio de la Clase 1 revisamos y mergeamos ese PR en vivo para confirmar que el flujo completo funciona.

### Flujo de Entregas Semanales (Fork + Pull Request)
1. Durante la cursada (Semanas 1 a 11), cada alumno tiene su propia carpeta aislada dentro del repositorio del curso: `entregas/<tu-usuario-github>/`.
2. Cada semana trabajás en tu Fork, subís tus cambios antes del **jueves a las 23:59** y abrís un **Pull Request** contra el repositorio del curso (no se permite pushear directo ni mergear sin revisión).
3. Un evaluador automático (**GitHub Action**) verifica que solo hayas modificado tu carpeta y genera un resumen limpio de tu código modificado.
4. En la clase del fin de semana defendés tu código oralmente. Una vez aprobado, **el instructor mergea tu PR a `main`** y antes de la semana siguiente hacés **Sync fork + `git pull`** para que tu próximo PR muestre únicamente lo nuevo.

### Regla de Dudas Entre Semana ("Primero al Grupo")
Si te trabás de lunes a jueves, primero buscá en los recursos de la semana y **compartí la duda en el grupo** para destrabarse entre compañeros. Si nadie logra resolverlo, recién ahí arrobás al instructor enviando: (1) qué intentaste, (2) el código relevante y (3) el error exacto.

---

## 4. Contenidos del Programa (3 Fases — 12 Semanas)

### Clase 0: Entrada en Calor (Antes de la Semana 1)
- **Clase 0:** Instalación del entorno (VS Code, Node.js LTS, Git, GitHub), Fork del repositorio, **HTML semántico**, **Box Model**, primera tarjeta web con HTML + CSS y apertura de tu **primer Pull Request**.

### Fase 1: Lógica Pura en TypeScript y Web Básica (Semanas 1 a 4)
- **Semana 1:** Revisión y merge del PR de Clase 0, `Sync fork`, TypeScript vs. JavaScript, variables, tipos primitivos (`string`, `number`, `boolean`), **Scope**, **`null` vs. `undefined`**, condicionales (`if/else`) y bucles (`for`, `while`).
- **Semana 2:** Funciones tipadas, `interface` y *union types* modernos (sin `enum`), **valor vs. referencia**, arrays y objetos, lectura de archivos `JSON` reales (`fs.readFileSync` + `JSON.parse`) y métodos fundamentales (`.map()`, `.filter()`, `.find()`, `.forEach()`).
- **Semana 3:** **DOM (*Document Object Model*)**, eventos del navegador y DevTools (*Elements* + *Network*), **Event Loop conceptual**, arquitectura Web (Cliente vs. Servidor), protocolo HTTP (verbos, headers, códigos `200`, `400`, `401`, `404`, `500`), APIs REST, exploración con **Postman**, lectura básica de **OpenAPI / Swagger** y asincronía (`async/await`, `try/catch`, `fetch` primero en Node y luego en un esqueleto web).
- **Semana 4 — Examen Eliminatorio 1:** Lógica pura en TypeScript + consumo de API pública (en pseudocódigo tipado). **Al finalizar el examen, quienes aprueban presentan su idea de MVP en 5 líneas para validar el alcance antes de arrancar React.**

### Fase 2: React, Bases de Datos SQL y Persistencia (Semanas 5 a 8)
- **Semana 5:** Salto a React con Vite (`react-ts`), TypeScript y Tailwind CSS (kit mínimo de clases + **Responsive básico**). **DOM imperativo vs. React declarativo**, componentes, `props` tipadas, estado (`useState`), inmutabilidad y formularios controlados. Inicio del Proyecto Integrador (CRUD completo en memoria).
- **Semana 6:** **Arquitectura de bases de datos relacionales** vs. NoSQL. Modelado de entidades, relaciones `1:N` y `N:M`, normalización básica, `Primary Key (PK)`, `Foreign Key (FK)`, restricciones (`NOT NULL`, `UNIQUE`, `CHECK`), índices y **SQL Injection**. Escritura de SQL puro en Supabase (`CREATE TABLE`, `INSERT`, `SELECT`, `UPDATE`, `DELETE`, `JOIN`).
- **Semana 7:** Conexión del frontend en React con Supabase usando **Custom Hooks** y **TanStack Query** (`useQuery`, `useMutation`), **los 4 estados de toda UI** (*Loading, Empty, Error, Data*), manejo de variables de entorno (`.env`) y `.gitignore`.
- **Semana 8 — Examen Eliminatorio 2:** Modelado en SQL + CRUD persistente en React, TanStack Query y Supabase.

### Fase 3: Seguridad, Roles, Backend Propio y Emancipación del MVP (Semanas 9 a 12)
- **Semana 9:** Autenticación (Login / JWT) vs. Autorización (**roles `admin` y `usuario`**), **`localStorage` vs. `Cookies` (`HttpOnly`)**. Implementación de Supabase Auth, políticas *Row Level Security (RLS)* en SQL, vistas separadas (Panel Admin vs. Vista Usuario) y estado global con **Zustand**.
- **Semana 10:** Backend propio en Node.js + Express (TypeScript). Creación de endpoints propios, middlewares, CORS, validación en servidor (*nunca confiar en el cliente*), **Rate Limiting**, validación obligatoria de sesión JWT y roles (`Authorization: Bearer <token>`), pruebas aisladas y colecciones en **Postman**, y documentación de endpoints *(con mención y bonus opcional de **OpenAPI / Swagger**)*.
- **Semana 11:** Recorte de alcance de **MVP (*Minimum Viable Product*)**, **Emancipación del MVP** (extraés tu carpeta `mvp/` a **tu propio repositorio independiente** en GitHub), **Deploy** en producción (Vercel + Render) y **Dominios y DNS** (cómo registrar un dominio `.com.ar` en NIC Argentina o `.com`, configurar registros `A`/`CNAME` en Vercel y habilitar HTTPS/SSL para entregar un sistema vendible con dirección propia).
- **Semana 12 — Examen Final (Defensa del MVP):** Presentación del proyecto publicado en internet, auditoría de código y modificación en vivo.

---

## 5. Diccionario Obligatorio de la Industria

Además de escribir código, vas a poder explicar con tus propias palabras:
- **Web y Navegador:** Frontend, Backend, Base de Datos, **DOM (*Document Object Model*)**, **HTML semántico y Box Model**, **Responsive (*mobile-first*)**, **Event Loop conceptual**, HTTP (Request/Response, Status Codes), API, API REST, **Postman (cliente HTTP)**, **OpenAPI / Swagger**, CORS, `fetch` (y Axios como alternativa), **Dominio, DNS (`A` / `CNAME`) y HTTPS/SSL**.
- **Datos y React Moderno:** TypeScript vs. JavaScript, **Scope**, **`null` vs. `undefined`**, **Valor vs. Referencia**, JSON, CRUD, **Arquitectura relacional (DER / Normalización)**, SQL vs. NoSQL, PK/FK, Join, **DOM imperativo vs. React declarativo**, **los 4 estados de UI (*Loading, Empty, Error, Data*)**, Custom Hooks, *Server State* (TanStack Query) vs. *Client Global State* (Zustand / Redux).
- **Seguridad:** Autenticación vs. Autorización, Roles, JWT / Bearer Token, RLS, **`localStorage` vs. `Cookies` (`HttpOnly`)**, **SQL Injection**, validación en servidor (*nunca confiar en el cliente*), **Rate Limiting** y variables de entorno (`.env`).
- **Producto:** MVP, Deploy, Localhost vs. Producción, Git/GitHub, Fork y Pull Request.

---

## 6. Proyecto Integrador (MVP Real y Vendible)

En la **Semana 4** proponés un problema real de un comercio o servicio local (o elegís una de las ideas recomendadas) y el instructor aprueba el alcance. El objetivo es que el sistema quede **completo, usable y vendible**, cumpliendo:
1. Mínimo **2–3 tablas relacionadas (`1:N`)** creadas en SQL a mano (`schema.sql`), incluyendo tabla de perfiles/roles.
2. **CRUD completo** en React + TypeScript + Tailwind + **Custom Hooks + TanStack Query + Zustand**.
3. **Panel de Administrador y Vista de Usuario/Cliente** con Login/Registro, gestión de **roles** y políticas **RLS** reales en PostgreSQL.
4. Al menos **1 o 2 endpoints propios en Node.js + Express** con validación de JWT y roles para reglas críticas de negocio o cierres/reportes, probados y documentados con **Postman** y `README.md`.
5. **Repositorio propio e independiente** (emancipado en Semana 11) y **desplegado en internet** con URL pública funcionando en celular y PC.

**Ideas recomendadas (vendibles a comercios/servicios locales):**
- **Sistema de Turnos y Reservas (Peluquería, Barbería, Estética o Cancha de Fútbol 5 / Pádel):** vista cliente para reservar horarios libres + panel admin para gestionar servicios, horarios y caja del día + validación antisolapamiento en Express.
- **Gestión de Gimnasio (Socios, Cuotas y Vencimientos):** vista socio para ver vencimiento de cuota y rutina + panel admin para cobrar cuotas mensuales, ver morosos y caja del mes + cálculo de vencimientos en Express.
- **Stock, Ventas y Cuentas Corrientes / Fiados (Despensa, Kiosco, Ferretería):** roles dueño/empleado, control de stock con alertas, libreta digital de cuentas corrientes/fiados y procesamiento de ventas + cierre de caja en Express.
- **Pedidos Online para Rotisería / Pizzería / Comida Casera:** menú público con carrito (Zustand) y seguimiento de estado + panel de cocina/dueño para pausar platos y avanzar pedidos + validación de totales en Express.

---

## 7. Sistema de Evaluación y Política de IA

- **Escala:** 1 al 10. **Nota mínima para aprobar cada examen:** **7**.
- **Formato de exámenes (Semanas 4, 8 y 12 — bloque de 2 horas):**
  - **40 % Pseudocódigo Tipado en Vivo (40 min, en simultáneo):** Todos reciben un problema real al mismo tiempo y deben **plantear y resolver la lógica en pseudocódigo estructurado** (sin IA), siendo **estrictos con los tipos, interfaces, estructuras de datos, validaciones y casos borde** — el foco es pensar y diseñar la solución con criterio técnico, no memorizar sintaxis.
  - **30 % Oral / Conceptual individual (15 min c/u):** Preguntas directas sin apuntes para validar comprensión real.
  - **30 % Entregable:** Avance del proyecto subido por PR en tiempo y forma, funcionando.
- **Política de IA durante la semana:** Podés usar herramientas de IA (ChatGPT, Claude, etc.) para destrabarte, entender errores o estudiar, **siempre declarando con honestidad en la plantilla del PR en qué te ayudó**. Sin embargo, que el código funcione no alcanza: si en la revisión no sabés explicar puntualmente qué hace una función, por qué funciona y el concepto detrás, el entregable vale **0**.

---

## Anexo Opcional — Acuerdo de Compromiso

> *Este curso es un espacio gratuito y armado a medida para que aprendas a programar en serio y termines con un proyecto propio desplegado y vendible. Para que valga el tiempo de todos, acordamos estas reglas simples:*
>
> 1. **Constancia y entregas:** Las clases del fin de semana son cortas (2 a 4 hs) porque el aprendizaje real pasa en la práctica de la semana (6 a 8 hs). Llegar **dos semanas seguidas sin la entrega hecha** o faltar sin avisar con **24 hs de anticipación** da por terminada la cursada.
> 2. **Consultas entre semana:** Primero al grupo para ayudarse entre compañeros; al instructor solo con error exacto, código y qué probaron.
> 3. **Honestidad con la IA:** Usala para aprender y declaralo en el PR; nunca entregues código que no puedas explicar.
> 4. **Exámenes eliminatorios:** Si en uno de los 3 exámenes sacás menos de 7, tenés **un único recuperatorio privado 1-a-1 a los 3 días** sobre la parte desaprobada. Si volvés a desaprobar, se cierra la cursada ahí, sin rencores — la amistad sigue igual.
