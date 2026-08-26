# AGENTS.md

## Qué es este proyecto

Demo comercial de una sola página (`index.html`) para un salón de belleza
real, "Sala de Belleza Lily". Es un sitio estático sin build step, pensado
para enseñarse al dueño del negocio como propuesta de página web.

## Arquitectura

- `index.html` — todas las secciones en un solo documento (hero, servicios,
  galería, sobre nosotras, horarios, opiniones, contacto/mapa, footer).
- `css/style.css` — un solo archivo de estilos, organizado por sección con
  comentarios de bloque (`/* ===== SECCIÓN ===== */`). Usa variables CSS en
  `:root` para la paleta y tipografías; no hay preprocesador.
- `js/script.js` — vanilla JS sin dependencias: menú móvil, animaciones de
  aparición con `IntersectionObserver` (atributo `data-reveal` en el HTML),
  y botón flotante "volver arriba".
- `images/` — fotografías reales recortadas de capturas de pantalla de
  Google Maps (se les quitó la interfaz del teléfono con ImageMagick).
- `netlify.toml` — publish = "." y cache headers para `/images/*`.

## Restricción de contenido (no obvia)

Toda la información visible (dirección, horarios, servicios, opiniones)
viene literalmente de capturas de la ficha de Google Maps del negocio. No
se debe inventar ni completar con datos genéricos (teléfono, WhatsApp,
redes sociales, precios) que no aparecían en el material original — si se
agregan en el futuro, deben venir confirmados por el dueño del negocio.

## Convenciones

- Sin frameworks de CSS ni JS; mantener el sitio 100% estático.
- Las animaciones deben limitarse a `transform`/`opacity` (ver guía de
  rendimiento aplicada en `style.css`).
- Las nuevas fotos deben pasar por el mismo flujo de recorte/optimización
  (`convert ... -resize 1400x -quality 82`) antes de entrar a `images/`.
- Mantener el diseño mobile-first: revisar breakpoints en `style.css`
  (`@media (max-width: 980px)` y `@media (max-width: 720px)`) al añadir
  secciones nuevas.
