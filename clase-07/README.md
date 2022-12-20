# HTML, SVG y CSS

### Clase 08 → 26/09/2022

**Para retomar el avance, aprovechemos las tres mejores calificaciones**: 

| Nombre | URL  | Nota |
|:-------|:-----|:-----:|
| KARINA ANACONA TOLOZA	| https://xnxconx.github.io/Prueba01/ | 7,0 |
| MARÍA JESÚS VIDAL	| https://mjvidallynch.github.io/infodigital-clase-06/	| 7,0 |
| VALENTINA WALLER QUEZADA	| https://valewq.github.io/InfoPrueba1/	 | 7,0 |

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

- - - - - -

**Ahora enfoquémonos en el [SVG](https://developer.mozilla.org/es/docs/Web/SVG/Element) con ["ingeniería inversa"](https://es.wikipedia.org/wiki/Ingenier%C3%ADa_inversa)**

En la [clase 04](https://github.com/profesorfaco/dno075-2023-1/tree/main/clase-04) referimos a 7 trabajos infografías publicadas por el South China Morning Post. La selección se basó en la accesibilidad de sus versiones [impresa](https://multimedia.scmp.com/culture/article/SCMP-printed-graphics-memory/) y [digital](https://www.scmp.com/infographic/).

Aprovechando esta accesibilidad, revisaremos algunas líneas de código fuente:

Partamos con **líneas 87 y 88 en el código fuente de [Godzilla: evolution of a monster](https://multimedia.scmp.com/infographics/culture/article/3012245/godzilla/index.html)**. 

Allí podemos rescatar un SVG: https://multimedia.scmp.com/infographics/culture/article/3012245/godzilla/svg/gojira.svg

Además del párrafo que dice: 

> Godzilla's name is a transliteration of <i>Gojira</i> (ゴジラ), a combination of two Japanese words: <i>gorira</i> (ゴリラ), meaning "gorilla", and <i>kujira</i> (鯨 or クジラ), meaning "whale"

Ahora vamos a las **líneas 151 y 152 en el código fuente de [China's wildlife trade
](https://multimedia.scmp.com/infographics/news/china/article/3064927/wildlife-ban/index.html)**, donde podemos encontrar dos versiones de una misma gráfica en SVG: 

- https://multimedia.scmp.com/infographics/news/china/article/3064927/wildlife-ban/svg/pangolin_facts.svg

- https://multimedia.scmp.com/infographics/news/china/article/3064927/wildlife-ban/svg/pangolin_phone.svg

En cada SVG se utiliza el elemento [`<image>`](https://developer.mozilla.org/en-US/docs/Web/SVG/Element/image). En tal elemento podemos encontrar un atributo `href` o `xlink:href`, que apunta a la URL de la imagen que se incluye dentro del SVG.

Aunque la imagen que se incluye dentro del SVG dice tener una extensión `.png`, lo que realmente se puede encontrar en su URL es una `.webp`, por lo que convendría googlear por un convertidor en línea de [WEBP a PNG](https://cloudconvert.com/webp-to-png), y luego reducir el peso del archivo convertido utilizando [TinyPNG](https://tinypng.com/).  

Sigamos con las **línea 108 y 109 del código fuente de [Bamboo scaffolding in Hong Kong](https://multimedia.scmp.com/infographics/culture/article/3183200/bamboo-scaffolding/index.html)**, donde vamos a rescatar otro par de gráficas en SVG:

- https://multimedia.scmp.com/infographics/culture/article/3183200/bamboo-scaffolding/svg/plant-d.svg

- https://multimedia.scmp.com/infographics/culture/article/3183200/bamboo-scaffolding/svg/plant-m.svg

Y terminemos con las **líneas 161 y 164 en el código fuente de [Why your smartphone is causing you ‘text neck’ syndrome](https://multimedia.scmp.com/lifestyle/article/2183329/text-neck/)**, rescatando: 

- https://multimedia.scmp.com/lifestyle/article/2183329/text-neck/svg/problems-m.svg

- https://multimedia.scmp.com/lifestyle/article/2183329/text-neck/svg/problems.svg

**Con todo lo que revisado, corresponde completar el `index.html` en esta carpeta**, que pueden ver como:

- [resultado](https://profesorfaco.github.io/dno075-2023-1/clase-08/) (gracias a [GitHub Pages](https://docs.github.com/es/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site))

- [código fuente](https://github.com/profesorfaco/dno075-2023-1/blob/main/clase-08/index.html)


- - - - - - - - - - - - -


###### [← CLASE PASADA](https://github.com/profesorfaco/dno075-2023-1/tree/main/clase-06) — [CLASE SIGUIENTE →](https://github.com/profesorfaco/dno075-2023-1/tree/main/clase-08) 
