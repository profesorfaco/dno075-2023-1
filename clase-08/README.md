# HTML, SVG y CSS

### [Infografía Digital, 6ta. versión](https://github.com/profesorfaco/dno075-2023-1#readme) → Clase 08 → 26/09/2022

Ya hemos trabajado con HTML, CSS y SVG. El primero es un lenguaje que nos permite describir los cotenidos de una página web. El segundo describe los aspectos de tales contenidos. Y el tercero es un lenguaje que [describe imágenes mediante fórmulas matemáticas basadas en puntos y líneas en una cuadrícula](https://www.adobe.com/cl/creativecloud/file-types/image/vector/svg-file.html). 

Sobre SVG corresponde recordar que:

- Trata el texto como tal, razón por la que los lectores de pantalla pueden escanear cualquier palabra incluida en las imágenes SVG, lo que resulta especialmente útil para las personas que necesiten ayuda con la lectura de los sitios web. Los motores de búsqueda también pueden leer e indexar el texto de las imágenes SVG.

- Siempre mantiene su resolución, independientemente de lo grandes o pequeños que se haga. 

- Suele ser más pequeño que una imagen rasterizada, que se describe el color de cada pixel en una cuadrícula, en lugar de emplear algoritmos matemáticos.

Aunque SVG suele ser más pequeño que una imagen rasterizada (.GIF, .JPG, .PNG., .WebP o .AVIF.), no siempre lo es; porque su tamaño dependerá de la concisión de sus descripciones, la ausencia de información que no sea relevante para la presentación de la imagen, y el buen uso de la vinculación (y nunca inscrustación) de recursos externos.

Es una muy mala idea trabajar en Adobe Illustrator con una imagen rasterizada de fondo, que se incrusta para luego [calcar](https://helpx.adobe.com/cl/illustrator/using/image-trace.html), luego guardarla con SVG y sin mediar revisión del código, ponerla en línea. 

La mala idea cambiaría, para mejor, si dejamos la imagen rasterizada como tal (vinculada) y revisamos el código con [SVG Minifier](https://www.svgminify.com/)

El servicio de [SVG Minifier](https://www.svgminify.com/) ofrece a la imagen vectorizada algo como lo que [TinyPNG](https://tinypng.com/) ofrece a la rasterizada.

Sea que usemos una imagen rasterizada o una vectorizada (SVG), o una rasterizada dentro de una vectorizada (SVG), nos corresponde cuidar el uso de las dimensiones justas y necesarias, además de una descripción hecha o modificada para pesar menos.

Las imágenes rasterizadas o vectorizadas pueden servir de soporte a nuestras gráficas figurativas, no figurativas o mixtas. Gráficas en las que nos corresponde cuidar los tamaños de los elementos mediante el intercambio de alternativas para pantallas más angostas o más anchas, y en todo tamaño de pantalla no corresponde cuidar los colores: Conviene evaluar el contraste figura/fondo en las gráficas con el uso de [Contrast Checker](https://webaim.org/resources/contrastchecker/), lo que vendría después de asegurarse que el esquema de color sea "colorblind safe" según [Color Brewer 2.0](https://colorbrewer2.org/) (es que un rojo y un verde pueden tener suficiente contraste con un fondo blanco, pero [no ser diferenciables entre sí](https://twitter.com/chiuminatto/status/1565323331946946562) bajo ciertas condiciones que podrían ver en sus propios navegadores Chrome, usando [Daltonize](https://chrome.google.com/webstore/detail/daltonize/obcnmdgpjakcffkcjnonpdlainhphpgh))

Yendo más allá de las imágenes, también nos corresponde:

- cuidar las redacciones de texto con atención a algunos artículos y videos en la [sección "Writing for the Web" del NN Group](https://www.nngroup.com/topic/writing-web/); un artículo que debería conocerse es **el viejo [How Users Read on the Web (Nielsen, 1997)](https://www.nngroup.com/articles/how-users-read-on-the-web/)**, y tal conocimiento podría complementarse con [How People Read Online: New and Old Findings (Moran, 2020)](https://www.nngroup.com/articles/how-people-read-online/). 

- evaluar la accesibilidad de cada infografía digital con **[WAVE de WebAIM](https://wave.webaim.org/)**.

- analizar performance, accesibilidad, buenas prácticas y posicionamiento en buscadores (Search Engine Optimization; SEO) con **[Google Lighthouse](https://blog.interdominios.com/google-lighthouse/)**.

En el análisis de LightHouse no alcanzaremos el 100 en SEO con lo que hemos revisado. Para poder alcazarlo, habría que agregar algunas líneas de código junto a las que habitualmente incluímos entre etiquetas `<head>` y `</head>`:

```
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>El título</title>
<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha2/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-aFq/bzH65dt+w6FI2ooMVUpc+21e0SRygnTpmBvdBgSdnuTN7QbdgL+OapgHtvPp" crossorigin="anonymous" />
```

Las líneas por agregar pueden ser generadas con los servicios de **[Meta Tags](https://metatags.io/)** o **[Mega Tags](https://megatags.co/)**. 

- - - - - - - - - - - - -


###### [← CLASE PASADA](https://github.com/profesorfaco/dno075-2023-1/tree/main/clase-07) — [CLASE SIGUIENTE →](https://github.com/profesorfaco/dno075-2023-1/tree/main/clase-10) 
