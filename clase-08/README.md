# HTML, SVG y CSS

### [Infografía Digital, 6ta. versión](https://github.com/profesorfaco/dno075-2023-1#readme) → Clase 08 → 25/04/2023

Ya hemos trabajado con HTML, CSS y SVG. Estamos aprovechando [Bootstrap 5](https://getbootstrap.com/) para acortar camino en el uso de HTML y CSS.

**HTML** es un lenguaje que nos permite **describir los contenidos de una página web**. **CSS describe los aspectos de tales contenidos**. Y **SVG describe el contenido de una imagen vectorizada basándose en XML** (por eso se parece tanto a HTML, y por este parecido sus aspectos también pueden ser descritos con CSS). 

Sobre **SVG** corresponde recordar que:

- **Trata el texto como tal**, razón por la que los lectores de pantalla pueden escanear cualquier palabra incluida en las imágenes SVG, lo que resulta especialmente útil para las personas que necesiten ayuda con la lectura de los sitios web. Los motores de búsqueda también pueden leer e indexar el texto de las imágenes SVG.

- **Siempre mantiene su resolución**, independientemente de lo grandes o pequeños que se haga (si necesitamos que se haga más grande o pequeño según el contexto, el `svg` debe tener un `viewBox` en lugar de `height` y `width` fijos).

- **Suele ser más ligero que una imagen rasterizada** (la descripción de la segunda suele ser más pesada porque debe referir al color de cada pixel que la compone).

Y hay más para recordar en [Información sobre archivos SVG | Adobe](https://www.adobe.com/cl/creativecloud/file-types/image/vector/svg-file.html)
 
- - - - - - - - - -

**Aunque SVG suele ser más pequeño que una imagen rasterizada (.GIF, .JPG, .PNG., .WebP o .AVIF.), no siempre lo es. El tamaño del SVG dependerá de la concisión de sus descripciones, la ausencia de información que no sea relevante para la presentación de la imagen, y el buen uso de la vinculación (y nunca inscrustación) de otras imágenes**.

Para ejemplificar lo recién dicho: Es una muy mala idea trabajar en Adobe Illustrator con una imagen rasterizada de fondo que se incrusta para [calcar](https://helpx.adobe.com/cl/illustrator/using/image-trace.html) (lo que podría generar demasiados trazados y puntos de anclaje), luego guardarla como SVG y, sin mediar revisión del código, ponerla en línea. La mala idea cambiaría, para aligerarse mucho, si dejamos la imagen rasterizada como tal (vinculada) y revisamos el código con [SVG Minifier](https://www.svgminify.com/).

[SVG Minifier](https://www.svgminify.com/) descarta información irrelevante, pero no elimina los espacios en blanco como sí lo hace [SVG Minify](https://coderstoolbox.online/toolbox/svg-minify).

[SVG Minifier](https://www.svgminify.com/) y [SVG Minify](https://coderstoolbox.online/toolbox/svg-minify) ofrecen a la imagen vectorizada algo como lo que [TinyPNG](https://tinypng.com/) ofrece a la rasterizada.

Sea que usemos una imagen rasterizada o una vectorizada (SVG), o una rasterizada dentro de una vectorizada (SVG), nos corresponde cuidar el uso de las dimensiones justas y necesarias, además de una descripción hecha o modificada para pesar menos.

- - - - - - - - - -

**Las imágenes rasterizadas o vectorizadas pueden servir de soporte a las gráficas figurativas, no figurativas o mixtas** que pueden ser parte de una infografía digital. 

**En estas gráficas nos corresponde cuidar el tamaño de los elementos que deben verse o leerse mediante alternativas para pantallas más angostas o más anchas. Y en toda alernativa nos corresponde cuidar los colores** mediante: 

- Evaluación del contraste figura/fondo con el uso de [Contrast Checker](https://webaim.org/resources/contrastchecker/)
 
- Uso de esquemas cromáticos que sean "colorblind safe" según [Color Brewer 2.0](https://colorbrewer2.org/) 

- Visualización de nuestras gráficas a través de simuladores de daltonismo, tales como [Daltonize](https://chrome.google.com/webstore/detail/daltonize/obcnmdgpjakcffkcjnonpdlainhphpgh)

- - - - - - - - - -

Yendo más allá de las gráficas y formatos de imagen que les ofrecen soporte, **en la infografía digital también nos corresponde**:

- **cuidar las redacciones de texto** con atención a algunos artículos y videos en la [sección "Writing for the Web" del NN Group](https://www.nngroup.com/topic/writing-web/); un artículo que debería conocerse es **el viejo [How Users Read on the Web (Nielsen, 1997)](https://www.nngroup.com/articles/how-users-read-on-the-web/)**, y tal conocimiento podría complementarse con [How People Read Online: New and Old Findings (Moran, 2020)](https://www.nngroup.com/articles/how-people-read-online/) 

- **evaluar la accesibilidad** con [WAVE de WebAIM](https://wave.webaim.org/)

- **analizar performance, accesibilidad, buenas prácticas y posicionamiento en buscadores (Search Engine Optimization; SEO)** con [Google Lighthouse](https://blog.interdominios.com/google-lighthouse/)

- **ofrecer la mejor presentación posible a los buscadores y usuarios de redes sociales, cuidando los metadatos** con una de estas alternativas: https://metatags.io/ o https://megatags.co/

- - - - - - - - - - 

#### AYUDA

**Utilizaremos lo publicado en https://profesorfaco.github.io/dno075-2023-1/clase-08/**

Es recomendable es que cada estudiante use [su cuenta en GitHub](https://github.com/) para:

1. [crear un repositorio](https://docs.github.com/es/get-started/quickstart/create-a-repo) con un nombre identificable (ej: `https://github.com/user/infodigital-clase-08`); y

2. [activar GitHub Pages](https://docs.github.com/es/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site) para poder ver su trabajo en línea, como página web construida con [HTML](https://developer.mozilla.org/es/docs/Learn/HTML/Introduction_to_HTML/Getting_started), a la que cualquiera accede por [HTTP](https://es.wikipedia.org/wiki/Protocolo_de_transferencia_de_hipertexto), después de apuntar a una dirección única ([URL](https://es.wikipedia.org/wiki/Localizador_de_recursos_uniforme)) (ej: `https://user.github.io/infodigital-clase-08`)


- - - - - - - - - - - - -


###### [← CLASE PASADA](https://github.com/profesorfaco/dno075-2023-1/tree/main/clase-07) — [CLASE SIGUIENTE →](https://github.com/profesorfaco/dno075-2023-1/tree/main/clase-10) 
