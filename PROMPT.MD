###  Prompt para Google Stitch

Copia y pega este texto exacto en Google Stitch. Está optimizado para forzar las restricciones de diseño (sin scroll) y preparar el código para tu arquitectura en Astro.

> **Prompt:**
> "Actúa como un desarrollador frontend experto. Necesito que generes el código HTML y CSS para una presentación de 11 diapositivas. El diseño debe ser estrictamente en una **paleta de colores oscura** (Dark Mode) y tener una estética tecnológica/moderna.
> 
> **Requisitos técnicos obligatorios:**
> 1. **Estructura modular:** Cada una de las 11 diapositivas debe estar envuelta en una etiqueta `<section>`.
> 2. **Sin Scroll (Viewport estricto):** El diseño de cada `<section>` debe estar pensado para ocupar exactamente el 100% de la pantalla (fullscreen) en formato horizontal (aspect ratio 16:9). No debe haber scroll vertical ni horizontal bajo ninguna circunstancia. Usa Flexbox o CSS Grid para centrar y distribuir el contenido internamente.
> 3. **Assets:** Incluye etiquetas `<img>` con placeholders que hagan referencia a imágenes tecnológicas (usa URLs de imágenes de prueba o deja el `src` preparado).
> 4. **Diapositiva 11 (Cierre):** La última diapositiva debe ser minimalista, conteniendo únicamente un mensaje de despedida y un contenedor preparado para incrustar un código `<svg>` directamente en el HTML (logo de la organización), perfectamente centrado.
> 5. **Entrega de Código:** Separa el código. Entrégame primero todo el HTML secuencial. Luego, entrégame el CSS limpio. No incluyas estilos al `body` ni uses estilos globales que rompan contenedores externos, asume que estas `<section>` vivirán dentro de un contenedor padre que ya gestiona la navegación."

 ---

### Prompt para conversión de Slides HTML a Componentes Astro (Reveal.js + Tailwind)

  Contexto del Proyecto:
  Estoy trabajando en una presentación con Astro y Reveal.js. Reveal.js está configurado para no escalar el contenido (width: '100%', height: '100%', margin: 0,
  minScale: 1, maxScale: 1), lo que significa que cada componente de diapositiva debe manejar su propio layout y ocupar todo el viewport para que Tailwind funcione
  correctamente.

  Tarea:
  Convierte el siguiente código HTML en un componente de Astro (.astro). El componente debe ser totalmente autónomo (self-contained) siguiendo esta estructura técnica
  estricta:

   1. Estructura Base: Todo el contenido debe estar envuelto en una etiqueta <section>.
   2. Scripts y Fuentes: Dentro de la etiqueta <section>, incluye los enlaces a fuentes de Google Fonts y el script de Tailwind CDN
      (https://cdn.tailwindcss.com?plugins=forms,container-queries). Usa is:inline en todos los scripts.
   3. Configuración de Tailwind: Define la configuración de Tailwind (tailwind.config) dentro de una función autoejecutable para evitar colisiones globales:

   1     <script is:inline>
   2         (function() {
   3             tailwind.config = { ... };
   4         })();
   5     </script>
   4. Estilos Aislados: Incluye un bloque <style is:inline> con los estilos CSS específicos del HTML. Debes añadir obligatoriamente esta clase para asegurar el layout:

   1     .slide-content {
   2         width: 100vw;
   3         height: 100vh;
   4         overflow: hidden;
   5     }
   5. Contenedor "Virtual Body": Inmediatamente después de los estilos, crea un div con la clase slide-content. Este div debe llevar todas las clases que originalmente
      estaban en la etiqueta <body> del HTML (ej: bg-background text-on-surface font-body-lg antialiased).
   6. Contenedor de Contenido: Dentro de slide-content, crea otro div con las clases h-full w-full flex items-center justify-center relative overflow-hidden + las
      clases que tuviera la etiqueta <section> original del HTML.
   7. Contenido Final: Inserta el contenido original (Progress Indicator, textos, imágenes, etc.) dentro de este último contenedor.

  Reglas de Oro:
   * Usa siempre is:inline para que Astro no procese ni mueva los scripts/estilos fuera del componente de la slide.
   * Mantén todos los colores, tipografías y espaciados definidos en el JSON de tailwind.config.
   * Asegúrate de que el "Progress Indicator" mantenga su estado (qué punto está iluminado) según el HTML original.

  Entrada (HTML):
  [PEGA AQUÍ EL CÓDIGO HTML]

  ---