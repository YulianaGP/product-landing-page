# 🧾 Documentación de la Página Web Estilo Apple

## ✅ Explicación de la estructura semántica (HTML5)

En el documento HTML que construí, apliqué una estructura semántica clara y coherente con las buenas prácticas de accesibilidad y jerarquía del contenido. Utilicé las siguientes etiquetas semánticas:

### 🧱 Estructura General

- **`<header>`**: Contiene el logotipo (SVG de Apple), el menú de navegación principal (`<nav>`) y los íconos de búsqueda y carrito. Esta sección está claramente separada como encabezado de la página.

- **`<main>`**: Aloja el contenido principal del sitio, dividido en secciones temáticas. Incluye:
  - `<section id="hero">`: Bloque destacado con título principal, descripción y botones de acción. Usé un `<h1>` como encabezado principal del sitio.
  - `<section class="caracteristicas">`: Presenta características clave del producto, con uso correcto de `<h2>` y `<h3>` para mantener la jerarquía.
  - `<section class="galaxi">`: Incluye información de envío y pagos. Ambas subsecciones (`#envio`, `#pago`) están bien divididas semánticamente.

- **`<footer>`**: Utilicé `<footer>` como sección final del sitio que incluye:
  - Información de contacto (email, teléfono, horarios),
  - Enlaces importantes como términos y condiciones,
  - Redes sociales con íconos accesibles (etiqueta `aria-label` y `<i>`).

### 🔤 Jerarquía de encabezados

- `<h1>` para el título principal.
- `<h2>` para secciones principales del `main`.
- `<h3>` para elementos dentro de listas o subsecciones, como cada característica del producto.

### ♿ Accesibilidad

- Imágenes con atributos `alt` descriptivos.
- Enlaces y botones con `aria-label` para navegadores de asistencia.
- Uso puntual de `role` sugerido en la documentación (`role="banner"` en `<header>`, `role="main"` en `<main>`, `role="contentinfo"` en `<footer>`), si se desea mejorar la experiencia para lectores de pantalla.

---

## 🤖 Prompt usado con IA (ChatGPT)

> “Te voy a enviar mi documento HTML y CSS para que me ayudes a verificarlo si está correctamente o no. Y qué se elimina o no o añadir en CSS. Además, ten en cuenta que las instrucciones de la tarea son: HTML5 Semántico (al menos 3 secciones semánticas: header, main, footer, jerarquía coherente de encabezados, evitar div innecesarios...), Accesibilidad (imágenes con alt, orden lógico del contenido, usar ARIA si se justifica), Estilos CSS Básicos (CSS reset, tipografía legible, contraste adecuado, etc.).”

---

## 🧪 ¿Cómo validé la respuesta?

### 1. Validación manual

- Revisé visualmente que las etiquetas fueran coherentes y bien organizadas.
- Comprobé que no había `div` innecesarios (todo tiene su rol semántico).
- Verifiqué que todas las imágenes tuvieran el atributo `alt`.

### 2. Validación con herramientas

- **[W3C Markup Validation Service](https://validator.w3.org/)**: Usé este validador para asegurarme de que el HTML estuviera bien formado.
- **Chrome Lighthouse**: Pasé una auditoría para comprobar accesibilidad, buenas prácticas y SEO.

### 3. Validación de contraste

- Verifiqué los colores claros sobre fondo negro con herramientas como [WebAIM Contrast Checker](https://webaim.org/resources/contrastchecker/) para asegurar un contraste mínimo de 4.5:1 en textos.

---

✅ Documento creado por [YulianaGP] para el proyecto de la página tipo Apple.

## Historias de usuario

### Ocultar el menu

Como usuario visualizando desde celular, deseo ver un icono donde muestre las opciones del menu, teniendo en cuenta que es una parte importante dentro de la pagina web.

### Página de testimonios

Como usuario, deseo ver una página aparte de testimonios organizada en una grilla con una barra superior (navbar) y un sidebar de filtros, para poder navegar y filtrar los comentarios fácilmente.

- Barra superior fija (o anclada) en la parte superior de la página.
- Sidebar a la izquierda en pantallas grandes y reacomodado debajo del navbar en pantallas pequeñas.
- Sección central que muestre los testimonios de forma clara (tarjetas o lista).
- El DOM debe mantener una estructura semántica (nav, aside, main).

### Página de compra

Como cliente, necesito acceder a una página de compra que incluya un layout con navbar y sidebar, para conocer los detalles del producto y finalizar mi adquisición de manera intuitiva

- Navbar en la parte superior para la navegación general.
- Sidebar con opciones o pasos de compra (e.g., selección de variantes, cálculo de envío, métodos de pago), aunque no sean funcionales aún.
- Sección principal para mostrar el resumen del producto y un formulario o botón para completar la compra (simulado).
- Responsividad: en pantallas pequeñas, el sidebar se reubica para no dificultar la visualización principal.

### Galeria de imágenes del producto

Como usuario, quiero ver una sección llamada ‘Galería de Imágenes’ con fotos del producto dispuestas en una cuadrícula flexible

### Layout Responsivo en Todas las Páginas

Como usuario que navega desde un teléfono, quiero que todas las páginas del sitio se adapten al ancho de mi dispositivo, evitando el scroll horizontal y manteniendo la accesibilidad.