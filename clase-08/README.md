# HTML, SVG y CSS

### [Infografía Digital, 6ta. versión](https://github.com/profesorfaco/dno075-2023-1#readme) → Clase 08 → 26/09/2022

Ya hemos trabajado con HTML, CSS y SVG. También hemos trabajado con imágenes rasterizadas, con formatos .GIF, .JPG o .PNG. A los que podríamos sumar formatos "next-gen" tales como .WebP o .AVIF. 

Sea que usemos una imagen rasterizada o una vectorizada (SVG), o una rasterizada dentro de una vectorizada (SVG), nos corresponde cuidar su peso mediante el uso de las dimensiones justas y necesarias, además de una descripción inteligente.

También nos corresponde:

- cuidar las redacciones de texto con atención a algunos artículos y videos en la [sección "Writing for the Web" del NN Group](https://www.nngroup.com/topic/writing-web/); un artículo que debería conocerse es **el viejo [How Users Read on the Web (Nielsen, 1997)](https://www.nngroup.com/articles/how-users-read-on-the-web/)**, y tal conocimiento podría complementarse con [How People Read Online: New and Old Findings (Moran, 2020)](https://www.nngroup.com/articles/how-people-read-online/). 

- evaluar la accesibilidad de cada infografía digital con **[WAVE de WebAIM](https://wave.webaim.org/)**.

- evaluar el contraste figura/fondo en las gráficas (que WAVE no puede analizar) mediante **otra herramienta de WebAIM, su [Contrast Checker](https://webaim.org/resources/contrastchecker/)**; esto vendría después de asegurarse que el esquema de color sea "colorblind safe" según [Color Brewer 2.0](https://colorbrewer2.org/) (es que un rojo y un verde pueden tener suficiente contraste con un fondo blanco, pero [no ser diferenciables entre sí](https://twitter.com/chiuminatto/status/1565323331946946562) bajo ciertas condiciones que podrían ver en sus propios navegadores Chrome, usando [Daltonize](https://chrome.google.com/webstore/detail/daltonize/obcnmdgpjakcffkcjnonpdlainhphpgh))

- analizar performance, accesibilidad, buenas prácticas y posicionamiento en buscadores (Search Engine Optimization; SEO) con **[Google Lighthouse](https://blog.interdominios.com/google-lighthouse/)**.

- recordar que el análisis recién referido no alcanzará el 100 en SEO. 

Para poder alcanzar la mejor evaluación posibe en SEO, habría que agregar algunas líneas junto a las que habitualmente incluímos entre etiquetas `<head>` y `</head>`:

```
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>El título</title>
<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha2/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-aFq/bzH65dt+w6FI2ooMVUpc+21e0SRygnTpmBvdBgSdnuTN7QbdgL+OapgHtvPp" crossorigin="anonymous" />
```

Las líneas por agregar pueden ser generadas con los servicios de **[Meta Tags](https://metatags.io/)** o **[Mega Tags](https://megatags.co/)**. 

- - - - - - - - - - - - -


###### [← CLASE PASADA](https://github.com/profesorfaco/dno075-2023-1/tree/main/clase-07) — [CLASE SIGUIENTE →](https://github.com/profesorfaco/dno075-2023-1/tree/main/clase-10) 
