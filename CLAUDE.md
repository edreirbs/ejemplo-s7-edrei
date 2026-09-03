# CLAUDE.md

Este archivo lo lee Claude cada vez que trabaja en esta carpeta, sin que se lo pidas.

---

## 1. Qué es este proyecto y quién lo usa

Es un buzón de sugerencias para la cena de fin de año de mi equipo. Lo uso yo
y todo mi equipo para juntar ideas de lugar, comida y actividades.

## 2. De dónde sale cada cifra

Los datos de esta página viven en el proyecto de Supabase **`lexi`**, en dos
tablas. Ninguna cifra ni ningún texto que se muestre se escribe a mano en el
HTML: todo sale de esas tablas o de lo que la persona escriba en el formulario.

| Tabla | Columnas | Qué guarda |
|---|---|---|
| `propuestas_cena` | `id`, `lugar`, `propuesto_por`, `justificacion`, `creado_en` | Una fila por propuesta enviada |
| `propuestas_cena_votos` | `propuesta_id`, `votante_id`, `creado_en` | Un voto por persona y propuesta |

El número de votos que ve la gente no es una columna: se cuenta sobre las filas
de `propuestas_cena_votos`. El `votante_id` es un identificador aleatorio que se
guarda en el navegador de cada quien; sirve para no votar dos veces la misma
propuesta, no es una cuenta de usuario.

La tabla `registros` existe en ese mismo proyecto de Supabase pero **no la usa
esta página**.

## 3. Cómo quiero que trabajes aquí

- Antes de un cambio grande, dame el plan por escrito y espera mi visto bueno.
- Un cambio a la vez. Enséñame qué cambió antes de escribirlo.
- Trabaja siempre en una rama, nunca directo sobre `main`.
- Cualquier cambio que se haga en cualquier rama se pide en pull request, se
  fusiona a `main` y se despliega automáticamente en producción de Netlify y
  de Supabase.
- **Si tienes acceso a mi base de datos, enséñame el SQL antes de correrlo y espera mi
  respuesta.** Crear o borrar tablas, agregar o quitar columnas y cambiar permisos no se
  deshacen con una rama: en cuanto corren, ya está.

## 4. Lo que nunca debes hacer

- **Nunca escribas en esta carpeta una llave que empiece con `sb_secret_` o que
  diga `service_role`.** La única llave que puede estar aquí es la que empieza
  con `sb_publishable_`, que está hecha para andar a la vista.
- No inventes datos. Si algo no está en la tabla, que la página diga que no hay
  nada todavía, no un ejemplo.
- No borres el historial ni fuerces cambios sobre lo ya publicado.

## 5. Mi regla de verificación

Cierro lo que entrego con: **haz pull y despliegue**. Antes de decir eso tiene
que ser cierto que el cambio ya está en la rama, que la vista previa de Netlify
lo muestra bien, y que nada de lo que se ve en pantalla está inventado: todo
sale de las tablas de la sección 2 o del formulario.

## 6. Cómo vuelvo a abrir esto

- El proyecto vive en el repositorio de GitHub `edreirbs/ejemplo-s7-edrei`.
- Se abre pidiéndole a Claude una sesión sobre este repo; no hace falta descargarlo.
- La página publicada está en <https://ejemplo-s7-edrei.netlify.app>.
  El tablero de Netlify está en <https://app.netlify.com/projects/ejemplo-s7-edrei>.
- La base de datos está en supabase.com, en el proyecto **`lexi`** de esta cuenta.

> **Si la página deja de mostrar datos después de una semana sin usarla**, casi
> siempre es que el proyecto gratuito de Supabase se pausó. Se despierta con el
> botón **Resume project**.

## 7. Sistema de diseño

- **Colores:** rojo, negro y blanco.
- **Tipografía:** Roboto.
