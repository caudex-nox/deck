<p align="center">
  <img src="public/deck.svg" width="200" alt="Deck">
</p>

# Deck · Presentaciones Web & Templates

**Deck** es un sistema para crear presentaciones y diapositivas en formato web moderno utilizando **Astro** y **Reveal.js**. 

El proyecto adopta un enfoque de desarrollo web tradicional y modular: cada diapositiva se construye como un componente reutilizable (`.astro`), lo que permite componer presentaciones de alto impacto visual, con soporte nativo para diseño responsivo, tipografías personalizadas y Tailwind CSS.

Además, el repositorio funciona como una **biblioteca de plantillas (templates)**: a través de distintas ramas y presentaciones especializadas (por ejemplo, presentaciones corporativas, técnicas o de producto), se exploran y conservan diferentes estilos estéticos para ser reutilizados en futuros decks.

---

## 🌟 Características

- **Formato Web Nativo:** Presentaciones accesibles desde cualquier navegador, con controles táctiles, por teclado, modo pantalla completa y vista general (*overview*).
- **Componentes Modulares:** Cada diapositiva es un componente independiente en `src/components/slides/`, facilitando el orden, versionado y reutilización.
- **Variedad de Estilos y Templates:** Diseños listos para usar y adaptar según la identidad visual de cada proyecto.
- **Rendimiento Ultrarrápido:** Construido con Astro, generando un empaquetado optimizado y sin sobrecarga innecesaria.

---

## 🚀 Inicio Rápido

El proyecto utiliza **pnpm** como gestor de paquetes. Ejecuta los siguientes comandos desde la raíz:

| Comando | Acción |
| :--- | :--- |
| `pnpm install` | Instala las dependencias del proyecto. |
| `pnpm dev` | Inicia el servidor de desarrollo en `localhost:4321`. |
| `pnpm build` | Compila la presentación estática para producción en `./dist/`. |
| `pnpm preview` | Previsualiza localmente el build de producción. |

---

## 📂 Estructura del Proyecto

```text
├── public/                  # Assets estáticos (logos, imágenes, favicon, fuentes)
├── src/
│   ├── components/
│   │   ├── slides/          # Diapositivas individuales (Slide01.astro, Slide02.astro...)
│   │   └── ui/              # Componentes de interfaz reutilizables (tarjetas, badges, etc.)
│   ├── layouts/
│   │   └── RevealLayout.astro # Contenedor principal: integra Reveal.js, navegación y estilos
│   └── pages/
│       └── index.astro      # Punto de entrada y orquestador del orden de las diapositivas
├── package.json
└── astro.config.mjs
```

---

## 🛠️ Cómo crear o modificar diapositivas

1. **Crear una diapositiva:**
   Añade un nuevo archivo en `src/components/slides/` (ejemplo: `Slide16.astro`).
   ```astro
   ---
   // Lógica o importaciones de componentes e iconos
   ---
   <section>
     <div class="slide-content flex items-center justify-center h-full w-full">
       <!-- Contenido de tu diapositiva -->
       <h1 class="text-3xl font-bold">Título de la Diapositiva</h1>
     </div>
   </section>
   ```

2. **Integrarla en la presentación:**
   Importa el componente en `src/pages/index.astro` y agrégalo en el orden deseado dentro de `<div class="slides">`:
   ```astro
   ---
   import Slide16 from "../components/slides/Slide16.astro";
   ---
   <RevealLayout>
     <div class="reveal">
       <div class="slides">
         <!-- ...slides anteriores -->
         <Slide16 />
       </div>
     </div>
   </RevealLayout>
   ```

---

## 🌿 Templates y Ramas

Para explorar o usar otros estilos y casos de uso, consulta las ramas disponibles en el repositorio (por ejemplo, `presentacion/innovacion`, `presentacion/caudex`), diseñadas para servir como base para nuevos proyectos de diapositivas.
