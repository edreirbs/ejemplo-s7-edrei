# Buzón de ideas para la cena de fin de año

Una página pública donde cualquiera puede proponer un lugar para la cena de fin
de año y votar las propuestas de los demás.

Construida en la **Sesión 7 del curso Claude for Business**, sin escribir código:
todo se le pidió a Claude en español.

## Cómo está armado

| Pieza | Qué hace |
|---|---|
| **GitHub** | Guarda este proyecto y su historial |
| **Netlify** | Publica lo que hay aquí como página web |
| **Supabase** | Guarda las propuestas y los votos (proyecto `lexi`) |

La página publicada está en <https://ejemplo-s7-edrei.netlify.app>.

## Cómo se cambia

1. Se abre una sesión de Claude sobre este repositorio.
2. Se le pide el cambio **en una rama**, no en `main`.
3. Se revisa el Pull Request y, cuando está bien, se fusiona a `main`.
4. Se le pide a Claude el despliegue. **Fusionar no publica por sí solo.**

> **Pendiente:** el sitio de Netlify todavía no está ligado al repositorio de
> GitHub, así que hoy cada publicación es un despliegue manual y no hay vistas
> previas por rama. Ligarlo se hace una sola vez desde el tablero de Netlify
> (*Project configuration → Build & deploy → Link a repository*); a partir de ahí
> cada rama tendría su vista previa y fusionar a `main` publicaría solo.

> **Publicar cuesta.** El plan gratuito de Netlify alcanza para unas veinte
> publicaciones al mes, así que conviene juntar cambios y publicar poco.

## Qué NO va en este repositorio

La llave `sb_publishable_` sí puede estar aquí: está hecha para andar a la vista.
La que empieza con `sb_secret_` o dice `service_role`, **nunca**.
