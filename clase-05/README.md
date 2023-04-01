# Infografías con SVG en HTML

### [Infografía Digital, 6ta. versión](https://github.com/profesorfaco/dno075-2023-1#readme) → Clase 05 → 04/04/2023

En esta clases vamos a aprovecharnos de partes de 3 trabajos infográficos publicados por el South China Morning Post (SCMP). Publicados no sólo una sino dos veces, con dos versiones, una impresa y otra digital.

**1. ANDAMIOS DE BAMBÚ**: 

- JUNE 28, 2022 - https://multimedia.scmp.com/infographics/culture/article/3183200/bamboo-scaffolding/index.html

- JUNE 30, 2022 - https://multimedia.scmp.com/culture/article/SCMP-printed-graphics-memory/lonelyGraphics/202206A309.html

**2. ANIMALES EN CHINA**:

- MARCH 4, 2020 - https://multimedia.scmp.com/infographics/news/china/article/3064927/wildlife-ban/index.html

- MARCH 5, 2020 - https://multimedia.scmp.com/culture/article/SCMP-printed-graphics-memory/lonelyGraphics/202003A250.html

**3. GODZILLA**:

- MAY 18, 2014 - https://multimedia.scmp.com/culture/article/SCMP-printed-graphics-memory/lonelyGraphics/201405A83.html

- MAY 29, 2019 - https://multimedia.scmp.com/infographics/culture/article/3012245/godzilla/index.html

**Es importante no confundir las partes con el todo. Recordemos que el análisis de una infografía no es lo mismo que el análisis de una gráfica (sea figurativa, no-figurativa o mixta)**.

Para recuperar el "todo" de las infografías digitales sobre [Bamboo scaffolding in Hong Kong](https://multimedia.scmp.com/infographics/culture/article/3183200/bamboo-scaffolding/index.html), [China’s wildlife trade](https://multimedia.scmp.com/infographics/news/china/article/3064927/wildlife-ban/index.html) y [Godzilla: evolution of a monster](https://multimedia.scmp.com/infographics/culture/article/3012245/godzilla/index.html) deben activar la opción *full-size* antes de tomar un pantallazo con https://www.site-shot.com/

Para recuperar las partes que nos interesan en las infografías digitales ya referidas, vamos al código fuente de cada una.

Partamos con las **líneas 108 y 109 del código fuente de [Bamboo scaffolding in Hong Kong](https://multimedia.scmp.com/infographics/culture/article/3183200/bamboo-scaffolding/index.html)**, donde podemos encontrar un par de gráficas en SVG:

- https://multimedia.scmp.com/infographics/culture/article/3183200/bamboo-scaffolding/svg/plant-d.svg

- https://multimedia.scmp.com/infographics/culture/article/3183200/bamboo-scaffolding/svg/plant-m.svg

Sigamos en el mismo código fuente, y avancemos a las **líneas 121 y 121**, donde podemos encontrar otro par de gráficas en SVG:

- https://multimedia.scmp.com/infographics/culture/article/3183200/bamboo-scaffolding/svg/poles-d.svg

- https://multimedia.scmp.com/infographics/culture/article/3183200/bamboo-scaffolding/svg/poles-m.svg

Cambiemos de infografía. Ahora vamos a **líneas 151 y 152** en el código fuente de [China’s wildlife trade](https://multimedia.scmp.com/infographics/news/china/article/3064927/wildlife-ban/index.html), donde podemos encontrar el siguiente par: 

- https://multimedia.scmp.com/infographics/news/china/article/3064927/wildlife-ban/svg/pangolin_facts.svg

- https://multimedia.scmp.com/infographics/news/china/article/3064927/wildlife-ban/svg/pangolin_phone.svg

Y en la infografía de [Godzilla: evolution of a monster](https://multimedia.scmp.com/infographics/culture/article/3012245/godzilla/index.html) revisaremos las líneas 102 y 103 para encontrar este par:

- https://multimedia.scmp.com/infographics/culture/article/3012245/godzilla/svg/legendary.svg

- https://multimedia.scmp.com/infographics/culture/article/3012245/godzilla/svg/legendary_m2.svg


Lo que tomamos en cada caso es un vínculo a un par de archivos SVG, que ofrecen dos opciones que serán intercambiables (en nuestro caso) gracias a [unas clases predefinidas de Bootstrap](https://getbootstrap.com/docs/5.3/utilities/display/).

Y en cada SVG podremos examinar el uso del elemento [\<image>](https://developer.mozilla.org/en-US/docs/Web/SVG/Element/image) 

Además de hacer tal examen, vamos a tomar íntegramente cada parte para traerla a nuestras carpetas de trabajo (y no estar tomándolas desde el servidor de SCMP):

- [resultado](https://profesorfaco.github.io/dno075-2023-1/clase-05/) (gracias a GitHub Pages)

- [código fuente](https://github.com/profesorfaco/dno075-2023-1/blob/main/clase-05/index.html)

- - - - - - - - - - 

###### [← CLASE PASADA](https://github.com/profesorfaco/dno075-2023-1/tree/main/clase-04) — [CLASE SIGUIENTE →](https://github.com/profesorfaco/dno075-2023-1/tree/main/clase-06) 

