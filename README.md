# Sala de Belleza Lily — Demo web

Sitio de demostración para **Sala de Belleza Lily**, un salón de belleza
ubicado en el Centro de Santiago Tianguistenco de Galeana, Méx. El objetivo
de este proyecto es mostrarle al negocio cómo se vería una página web
profesional, usando únicamente información y fotografías reales extraídas
de sus capturas de Google Maps.

## Tecnología

- HTML5 semántico
- CSS3 (variables custom, CSS Grid, animaciones al hacer scroll)
- JavaScript nativo (sin frameworks ni dependencias)
- Sitio 100% estático, sin backend ni build step

## Estructura del proyecto

```
.
├── index.html          # página única con todas las secciones
├── css/
│   └── style.css       # estilos del sitio
├── js/
│   └── script.js        # menú móvil, animaciones y botón "volver arriba"
├── images/              # fotografías reales del salón (recortadas de capturas de Maps)
└── netlify.toml          # configuración de despliegue en Netlify
```

## Contenido usado

Toda la información (nombre, dirección, horarios, servicios y opiniones)
proviene de capturas de pantalla de la ficha de Google Maps del negocio.
No se inventó ningún dato. El sitio no incluye botones de WhatsApp,
Facebook ni llamada telefónica porque esos datos no aparecían en las
imágenes proporcionadas; solo se incluye un botón de "Ver en Google Maps".

## Cómo verlo localmente

No requiere instalación. Basta abrir `index.html` en un navegador, o servir
la carpeta con cualquier servidor estático, por ejemplo:

```bash
npx serve .
```

## Despliegue en Netlify

El proyecto está listo para arrastrarse y soltarse en Netlify, o conectarse
como repositorio con el build configurado en `netlify.toml` (publish = ".").
