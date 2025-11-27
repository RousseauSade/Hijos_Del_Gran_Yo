# Sitio Web de la Iglesia "Hijos del Gran Yo Soy"

https://rousseausade.github.io/Hijos_Del_Gran_Yo/

Este proyecto contiene el código fuente para el sitio web oficial de la Iglesia Hijos del Gran Yo Soy. El sitio está diseñado para ser una plataforma moderna, acogedora y funcional para la comunidad, permitiendo el acceso a transmisiones en vivo, información de eventos y más.

## ✨ Características Principales

- **Diseño Responsivo:** Totalmente adaptable a computadoras de escritorio, tabletas y teléfonos móviles.
- **Transmisión Dinámica de YouTube:** Muestra automáticamente la transmisión en vivo del canal cuando está activa. Si no hay ninguna transmisión, muestra una lista con los últimos videos subidos para que la sección siempre tenga contenido.
- **Estilo Moderno y Cristiano:** Paleta de colores, tipografías y diseño visual orientados a crear una atmósfera de reverencia y calidez.
- **Navegación Intuitiva:** Menú de navegación claro y un menú "hamburguesa" en forma de cruz para dispositivos móviles.
- **Secciones Clave:**
  - **Bienvenida:** Mensaje de bienvenida con un botón de llamada a la acción.
  - **Transmisión en Vivo:** Reproductor de YouTube integrado.
  - **Galería:** Espacio para mostrar momentos de la comunidad.
  - **Eventos:** Lista de los próximos eventos de la iglesia.

---

## 📂 Estructura de Archivos

El proyecto se organiza de la siguiente manera:

- **`index.html`**: Es la página de inicio y la más importante. Contiene la mayoría de las secciones y el script para el reproductor de YouTube.
- **`nosotros.html`**: La página "Sobre Nosotros", donde se puede detallar la historia y misión de la iglesia.
- **`sermones.html`**: Una página dedicada a alojar sermones pasados, ya sea en formato de video o audio.
- **`style.css`**: La hoja de estilos central. Controla **toda** la apariencia visual del sitio (colores, fuentes, espaciados, animaciones, etc.).
- **`README.md`**: Este mismo archivo, que sirve como documentación del proyecto.

---

## 🚀 Configuración Inicial (¡Importante!)

Para que el reproductor de YouTube funcione correctamente, es **necesario** configurar una clave de API de YouTube.

1.  **Obtener una Clave de API:**
    - Ve a la Consola de Google Cloud.
    - Crea un nuevo proyecto (o selecciona uno existente).
    - En el menú de navegación, ve a `APIs y servicios > Biblioteca` y busca y activa la **"YouTube Data API v3"**.
    - Luego, ve a `APIs y servicios > Credenciales`.
    - Haz clic en `+ CREAR CREDENCIALES` y selecciona `Clave de API`.
    - **Copia la clave generada.** Es recomendable restringir la clave para que solo pueda ser usada en tu dominio web por seguridad.

2.  **Añadir la Clave al Código:**
    - Abre el archivo `index.html`.
    - Busca la siguiente línea de código casi al final del archivo:
      ```javascript
      const API_KEY = "AQUÍ_DEBES_COLOCAR_TU_API_KEY";
      ```
    - Reemplaza `"AQUÍ_DEBES_COLOCAR_TU_API_KEY"` por la clave que copiaste en el paso anterior.

Una vez hecho esto, el reproductor funcionará automáticamente.

---

## 🎨 Personalización

Puedes personalizar fácilmente el contenido y la apariencia del sitio:

- **Cambiar Colores y Fuentes:** Abre `style.css`. Al principio del archivo, encontrarás la sección `:root`. Puedes cambiar los valores de las variables (`--primary-color`, `--accent-color`, etc.) para modificar la paleta de colores de todo el sitio.

  ```css
  :root {
      --primary-color: #1a2a40; /* Azul noche profundo */
      --accent-color: #d4af37; /* Oro antiguo */
      /* ...otros colores... */
  }
  ```

- **Actualizar Eventos:** En `index.html`, busca la sección con `id="events"`. Puedes editar, añadir o eliminar los `div` con la clase `event-item` para actualizar la lista de eventos.

- **Cambiar Imágenes de la Galería:** En `index.html`, busca la sección con `id="gallery"`. Reemplaza las URLs en las etiquetas `<img>` por las rutas a tus propias imágenes.

- **Imagen de Fondo de Bienvenida:** En `style.css`, busca el selector `#welcome`. Puedes cambiar la URL en la propiedad `background` para poner tu propia imagen de fondo.

- **Enlaces a Redes Sociales:** En el `<footer>` (pie de página) de cada archivo `.html`, actualiza los enlaces (`href="#"`) dentro de la clase `.social-links` para que apunten a tus perfiles reales.
