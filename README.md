# Las Feliipas

Sitio web premium de café & pastelería en La Plata. Diseño cinematográfico, mínimo y editorial — inspirado en Surry Hills Coffee, Felix Roasting Co y Ninina Bakery.

**Av. 53 e/ 16 y 17 · La Plata · Lun–Vie 08:30 — 19:30**
**[@lasfeliipas](https://instagram.com/lasfeliipas)**

---

## Stack

- HTML / CSS / JavaScript vanilla (sin frameworks, sin build step)
- [Lenis](https://github.com/darkroomengineering/lenis) para smooth scroll
- Google Fonts: Cormorant Garamond · Raleway · Space Mono

## Estructura

```
.
├── index.html        # SPA completa (HTML + CSS + JS)
├── img/              # Productos, branding, hero, nosotros
│   ├── salado/
│   ├── pasteleria/
│   ├── cafe/
│   ├── bebidas/
│   ├── nosotros/
│   ├── hero/
│   └── branding/
├── package.json      # Dependencia única: lenis
└── .claude/launch.json  # Config del dev server (preview)
```

## Secciones

1. **Hero** — Imagen full-bleed con ken-burns parallax
2. **Editorial strip** — Café · Pastelería · Tartas & mesa
3. **Nosotros** — Historia + slideshow mini
4. **Menú** — Tabs por categoría, carrito con WhatsApp checkout
5. **Divider** — Full-bleed cinematográfico
6. **Galería** — Velocity gallery 3D horizontal (auto-scroll, drag, wave tilt, scramble text)
7. **Visita** — Mapa embebido + horarios + dirección
8. **Footer** + Social rail fijo

## Features clave

- **Topbar marquee**: ticker infinito con animación JS rAF (bypassea `prefers-reduced-motion`)
- **Velocity gallery**: carrusel 3D con 37 productos, drag con momentum, tilt en eje Y como ola según scroll velocity, hover con scramble text, vignette en bordes
- **Cart FAB**: botón flotante con thumbnails de productos agregados, total y count, animado por rAF
- **Reveal on scroll**: animaciones por JS rAF (también bypassea `prefers-reduced-motion`), staggered, con variantes blur
- **WhatsApp checkout**: el pedido se envía pre-formateado por WhatsApp Business

## Cómo correrlo localmente

```bash
# Instalar Lenis
npm install

# Servir estático (cualquier server estático sirve)
npx serve -l 3456 .

# Abrir en el browser
# http://localhost:3456
```

## Paleta

| Variable     | Color    | Uso                      |
|--------------|----------|--------------------------|
| `--ivory`    | `#f4ede0`| Fondo principal cálido   |
| `--forest`   | `#1f2a22`| Verde oscuro acento      |
| `--copper`   | `#a26a3a`| Marrón cobre CTA         |
| `--ink`      | `#1a1815`| Negro tipográfico        |

## Tipografía

- **Display**: `Cormorant Garamond` (italic, headlines)
- **Body**: `Raleway` (sans, UI)
- **Mono**: `Space Mono` (eyebrows, labels editoriales)

## Notas

- El sitio es una SPA en un solo archivo `index.html` (~130 KB).
- Todas las animaciones usan `requestAnimationFrame` para que funcionen incluso con `prefers-reduced-motion` activo en el OS — Chrome pinea las CSS transitions cuando esa preferencia está habilitada.
- Las imágenes están optimizadas localmente; no hay CDN.

---

© Las Feliipas
