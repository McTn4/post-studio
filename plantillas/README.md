# Plantillas — Post Studio

Cinco modelos de web genéricos (no atados a ningún sector) pensados para enseñar
en redes sociales y para usar como base de proyectos reales.

Abre `index.html` para ver la galería con vistas previas en vivo.

| # | Modelo | Idea | Efectos principales |
|---|---|---|---|
| 01 | [Cinema](01-cinema.html) | Lanzamiento de producto, tema oscuro | Secuencia cinematográfica controlada por scroll, tarjeta que se abre a pantalla completa, mockup 3D con paralaje, contador y anillo animados |
| 02 | [Constellation](02-constellation.html) | Técnico y preciso, tema oscuro | Malla interactiva en canvas con física de resortes, cursor automático cuando nadie interactúa, revelado del titular letra a letra |
| 03 | [Aurora](03-aurora.html) | Editorial y cálido, tema claro | Degradados vivos, revelado de texto por líneas, cursor propio, botones magnéticos, tarjetas apiladas, acordeón |
| 04 | [Monolith](04-monolith.html) | Editorial rotundo, tema oscuro | Tipografía gigante con máscaras, galería que avanza en horizontal con el scroll vertical, previsualización flotante al pasar el cursor |
| 05 | [Prism](05-prism.html) | SaaS / producto, cristal y color | Paralaje 3D de paneles de cristal, foco de luz que sigue al cursor, tarjetas inclinables, precios con cambio mensual/anual animado |

## Cómo están hechas

- **Un solo archivo HTML por modelo.** HTML, CSS y JavaScript van dentro. No hay
  compilación, `node_modules` ni dependencias que se rompan con el tiempo.
- **Sin librerías.** Nada de GSAP, jQuery o frameworks: todo es CSS y JavaScript
  nativo (`IntersectionObserver`, `requestAnimationFrame`, `position: sticky`).
- **Único recurso externo:** las tipografías de Google Fonts. Si se quitan, cada
  plantilla cae en la fuente del sistema sin romperse.
- **Accesibilidad:** foco visible, estructura semántica, `aria-label` donde hace
  falta y desactivación completa del movimiento con `prefers-reduced-motion`.
- **Responsive** de 360 px hasta pantallas panorámicas.

## Cómo personalizar una plantilla

1. Abre el archivo y busca el bloque `:root { ... }` al principio del `<style>`.
   Ahí están el color de marca, los grises, el radio de las esquinas, el ancho
   máximo y las tipografías. Cambiando esas variables cambia toda la página.
2. Sustituye los textos directamente en el HTML.
3. El nombre de marca aparece en el `<nav>`, en el pie y (según el modelo) en el
   titular. Búscalo y reemplázalo.
4. Cambia el `<title>`, la `<meta name="description">` y el `favicon` en línea
   del `<head>`.

## Publicar

Cualquier hosting estático sirve. Con GitHub Pages basta con activar Pages sobre
la rama y entrar en `/plantillas/`.
