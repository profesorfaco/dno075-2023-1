# HTML, SVG y CSS

### [Infografía Digital, 6ta. versión](https://github.com/profesorfaco/dno075-2023-1#readme) → Clase 08 → 26/09/2022

**Para que tales infografía digitales mejoren aun más, conviene**:

- volver sobre las redacciones después de revisar algunos artículos y videos en la [sección "Writing for the Web" del NN Group](https://www.nngroup.com/topic/writing-web/); un artículo que debería conocerse es **el viejo [How Users Read on the Web (Nielsen, 1997)](https://www.nngroup.com/articles/how-users-read-on-the-web/)**, y tal conocimiento podría complementarse con [How People Read Online: New and Old Findings (Moran, 2020)](https://www.nngroup.com/articles/how-people-read-online/). 

- evaluar la accesibilidad a su infografía digital con **[WAVE de WebAIM](https://wave.webaim.org/)**.

- evaluar el contraste figura/fondo en las gráficas (que WAVE no puede analizar) mediante **otra herramienta de WebAIM, su [Contrast Checker](https://webaim.org/resources/contrastchecker/)**; esto vendría después de asegurarse que el esquema de color sea "colorblind safe" según [Color Brewer 2.0](https://colorbrewer2.org/) (es que un rojo y un verde pueden tener suficiente contraste con un fondo blanco, pero [no ser diferenciables entre sí](https://twitter.com/chiuminatto/status/1565323331946946562) bajo ciertas condiciones que podrían ver en sus propios navegadores Chrome, usando [Daltonize](https://chrome.google.com/webstore/detail/daltonize/obcnmdgpjakcffkcjnonpdlainhphpgh))

- analizar performance, accesibilidad, buenas prácticas y posicionamiento en buscadores (Search Engine Optimization; SEO) con **[Google Lighthouse](https://blog.interdominios.com/google-lighthouse/)**.

- el análisis recién referido no alcanzará el 100 en SEO, pero podríamos acercarnos a tal número con **[Meta Tags](https://metatags.io/)** o **[Mega Tags](https://megatags.co/)**.

Usemos **Meta** o **Mega** Tags, lo que corresponde aquí es volver al código fuente de documento HTML, aprendiendo que hay algo que nos falta incluir en su cabeza (en el [elemento HTML](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/Getting_started#anatomy_of_an_html_element) entre etiquetas `<head>…</head>`):

```
<!doctype html>
<html lang="es">
  <head>
    <!-- Datos-sobre-datos en el documento, título del documento, estilos, etc. -->
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <title>Reemplaza este título que se muestra en la ventana de tu navegador</title>
    <!-- Acá termina la cabeza del documento HTML -->
  </head>
  <body>
    <h1>¡Hola mundo!</h1>
  </body>
</html>
```

Si revisan la cabeza (`<head>…</head>`) de los documentos `index.html` preparados para cada clase ([01](https://github.com/profesorfaco/dno075-2023-1/blob/main/clase-01/index.html), [03](https://github.com/profesorfaco/dno075-2023-1/blob/main/clase-03/index.html), [04](https://github.com/profesorfaco/dno075-2023-1/blob/main/clase-04/index.html), [05](https://github.com/profesorfaco/dno075-2023-1/blob/main/clase-05/index.html) y [06](https://github.com/profesorfaco/dno075-2023-1/blob/main/clase-06/index.html)) podrán encontrar líneas que se repiten:

```
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-1BmE4kWBq78iYhFldvKuhfTAU6auU8tT94WrHftjDbrCEXSU1oBoqyl2QvZ6jIW3" crossorigin="anonymous" />
```

La primera línea indica que el documento utiliza el formato de codificación de [caracteres UTF-8](https://es.wikipedia.org/wiki/UTF-8).

La segunda línea le pide algo al navegador, que utilice todo el ancho del [viewport](https://developer.mozilla.org/en-US/docs/Web/HTML/Viewport_meta_tag).

La tercera vincula la [hoja de estilos de Bootstrap](https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/css/bootstrap.min.css) en su quinta versión.

Para complementar y/o contradecir lo que nos ofrece el CSS de [Bootstrap](https://getbootstrap.com/), es que abrimos un espacio dentro de la cabeza, para incrustar un lenguaje distinto del [HTML](https://developer.mozilla.org/es/docs/Learn/HTML/Introduction_to_HTML/Getting_started#%C2%BFqu%C3%A9_es_el_html).

```
<style>
/* aquí dentro se escribe en otro lenguaje: CSS */
selector {propiedad: valor;}
</style>
```

El lenguaje que incluímos es [CSS](https://developer.mozilla.org/es/docs/Learn/Getting_started_with_the_web/CSS_basics#entonces_%C2%BFqu%C3%A9_es_css_realmente). Lenguaje que también puede ser incluido dentro de un [SVG](https://developer.mozilla.org/es/docs/Web/SVG/Element): 

Revisen el código fuente de sus gráficas, y notarán que en las primeras líneas de cada SVG descargado de [RAWGraphs](https://app.rawgraphs.io/) y/o trabajado con Adobe Illustrator también tienen un `<style>…</style>`.

Usemos **Meta** o **Mega** Tags, lo que corresponde aquí es volver al código fuente de documento HTML, aprendiendo que hay algo que nos falta incluir en su cabeza (en el [elemento HTML](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/Getting_started#anatomy_of_an_html_element) entre etiquetas `<head>…</head>`):

```
<!doctype html>
<html lang="es">
  <head>
    <!-- Datos-sobre-datos en el documento, título del documento, estilos, etc. -->
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <title>Reemplaza este título que se muestra en la ventana de tu navegador</title>
    <!-- Acá termina la cabeza del documento HTML -->
  </head>
  <body>
    <h1>¡Hola mundo!</h1>
  </body>
</html>
```

Si revisan la cabeza (`<head>…</head>`) de los documentos `index.html` preparados para cada clase ([01](https://github.com/profesorfaco/dno075-2023-1/blob/main/clase-01/index.html), [03](https://github.com/profesorfaco/dno075-2023-1/blob/main/clase-03/index.html), [04](https://github.com/profesorfaco/dno075-2023-1/blob/main/clase-04/index.html), [05](https://github.com/profesorfaco/dno075-2023-1/blob/main/clase-05/index.html) y [06](https://github.com/profesorfaco/dno075-2023-1/blob/main/clase-06/index.html)) podrán encontrar líneas que se repiten:

```
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-1BmE4kWBq78iYhFldvKuhfTAU6auU8tT94WrHftjDbrCEXSU1oBoqyl2QvZ6jIW3" crossorigin="anonymous" />
```

La primera línea indica que el documento utiliza el formato de codificación de [caracteres UTF-8](https://es.wikipedia.org/wiki/UTF-8).

La segunda línea le pide algo al navegador, que utilice todo el ancho del [viewport](https://developer.mozilla.org/en-US/docs/Web/HTML/Viewport_meta_tag).

La tercera vincula la [hoja de estilos de Bootstrap](https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/css/bootstrap.min.css) en su quinta versión.

Para complementar y/o contradecir lo que nos ofrece el CSS de [Bootstrap](https://getbootstrap.com/), es que abrimos un espacio dentro de la cabeza, para incrustar un lenguaje distinto del [HTML](https://developer.mozilla.org/es/docs/Learn/HTML/Introduction_to_HTML/Getting_started#%C2%BFqu%C3%A9_es_el_html).

```
<style>
/* aquí dentro se escribe en otro lenguaje: CSS */
selector {propiedad: valor;}
</style>
```

El lenguaje que incluímos es [CSS](https://developer.mozilla.org/es/docs/Learn/Getting_started_with_the_web/CSS_basics#entonces_%C2%BFqu%C3%A9_es_css_realmente). Lenguaje que también puede ser incluido dentro de un [SVG](https://developer.mozilla.org/es/docs/Web/SVG/Element): 

Revisen el código fuente de sus gráficas, y notarán que en las primeras líneas de cada SVG descargado de [RAWGraphs](https://app.rawgraphs.io/) y/o trabajado con Adobe Illustrator también tienen un `<style>…</style>`.

**Con todo lo que revisado, corresponde completar el `index.html` en esta carpeta**, que pueden ver como:

- [resultado](https://profesorfaco.github.io/dno075-2023-1/clase-08/) (gracias a [GitHub Pages](https://docs.github.com/es/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site))

- [código fuente](https://github.com/profesorfaco/dno075-2023-1/blob/main/clase-08/index.html)


- - - - - - - - - - - - -


###### [← CLASE PASADA](https://github.com/profesorfaco/dno075-2023-1/tree/main/clase-07) — [CLASE SIGUIENTE →](https://github.com/profesorfaco/dno075-2023-1/tree/main/clase-10) 
