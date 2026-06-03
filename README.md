# DECK: Presentación interactiva

Este proyecto es una plantilla para crear presentaciones dinámicas utilizando **Astro** y **Reveal.js**. Permite desarrollar diapositivas como componentes individuales de Astro, facilitando la modularidad, el uso de componentes UI reutilizables y la integración con otras tecnologías web.

## 🚀 Inicio Rápido

Todos los comandos se ejecutan desde la raíz del proyecto.

| Comando        | Acción                                                |
| :------------- | :---------------------------------------------------- |
| `pnpm install` | Instala las dependencias del proyecto.                |
| `pnpm dev`     | Inicia el servidor de desarrollo en `localhost:4321`. |
| `pnpm build`   | Construye el sitio para producción en `./dist/`.      |
| `pnpm preview` | Previsualiza la versión compilada localmente.         |

## 📂 Estructura Principal

- **`src/pages/index.astro`**: el punto de entrada de la presentación donde se orquestan y ordenan las diapositivas.
- **`src/layouts/RevealLayout.astro`**: plantilla principal que inicializa Reveal.js y contiene los estilos globales de la presentación.
- **`src/components/slides/`**: carpeta destinada para crear cada diapositiva como un componente de Astro (`Slide01_Intro.astro`, etc.).
- **`src/components/ui/`**: componentes reutilizables a lo largo de las diapositivas (tarjetas, botones, etc.).

## 🛠️ ¿Cómo añadir una diapositiva?

1. Crea un nuevo componente `.astro` dentro de `src/components/slides/` (ej: `Slide01.astro`).
2. El componente debe estar envuelto en una etiqueta `<section>`.
3. Importa el componente en `src/pages/index.astro` y añádelo dentro del contenedor `<div class="slides">`.
