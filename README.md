# Buzón de ideas para la cena de fin de año

Página pública para que mi equipo proponga lugares para la cena de fin de año y
vote las propuestas de los demás. No hay que crear cuenta: quien tenga la liga
propone y vota. Está publicada en <https://ejemplo-s7-edrei.netlify.app>.

**De dónde salen los datos.** Nada de lo que se ve está escrito en el HTML. Las
propuestas salen de la tabla `propuestas_cena` del proyecto de Supabase `lexi`, y
los votos se cuentan sobre las filas de `propuestas_cena_votos`. El navegador las
lee con la llave `sb_publishable_` de `index.html`, que es pública a propósito. Si
la página sale vacía, casi siempre Supabase pausó el proyecto: **Resume project**.

**Qué hay en `.claude`.** Un subagente, `revisor-antes-de-publicar`: revisa el
repositorio antes de publicar y reporta llaves secretas, cambios de más y datos
inventados en el HTML. Solo reporta, no arregla nada. Se le llama diciendo
"revisa antes de publicar".

**Para continuar.** Abre una sesión de Claude sobre este repositorio y pídele el
cambio en español. Lee antes `CLAUDE.md`: ahí están las reglas de la casa (siempre
en una rama, nunca sobre `main`, todo pasa por un Pull Request) y cómo se publica.
