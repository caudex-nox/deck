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
