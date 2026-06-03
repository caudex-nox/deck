# Estructura del Proyecto: Presentaciones Astro + Reveal.js + Stitch

## Árbol de Directorios

```text
/
├── public/
│   ├── favicon.svg
│   └── assets/
│       ├── tech-bg.jpg         # Imágenes de fondo o assets tecnológicos
│       └── org-logo.svg        # Logo de la organización para el cierre
├── src/
│   ├── components/
│   │   ├── slides/             # Componentes específicos de cada diapositiva
│   │   │   ├── Slide01_Intro.astro
│   │   │   ├── Slide02_Contexto.astro
│   │   │   ├── ...
│   │   │   └── Slide11_Cierre.astro
│   │   └── ui/                 # Componentes UI reutilizables (si aplican)
│   │       └── TechCard.astro
│   ├── layouts/
│   │   └── RevealLayout.astro  # Configuración base de HTML y Reveal.js
│   └── pages/
│       └── index.astro         # Punto de entrada. Importa y orquesta las slides.
├── package.json
└── astro.config.mjs