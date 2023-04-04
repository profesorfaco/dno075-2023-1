# Infografías con SVG en HTML

### [Infografía Digital, 6ta. versión](https://github.com/profesorfaco/dno075-2023-1#readme) → Clase 05 → 04/04/2023

En esta clase vamos a aprovecharnos de partes de 3 trabajos infográficos publicados por el South China Morning Post (SCMP). Publicados no sólo una sino dos veces, con dos versiones, una impresa y otra digital.

**1. Bamboo scaffolding in Hong Kong**: 

- JUNE 28, 2022 - https://multimedia.scmp.com/infographics/culture/article/3183200/bamboo-scaffolding/index.html

- JUNE 30, 2022 - https://multimedia.scmp.com/culture/article/SCMP-printed-graphics-memory/lonelyGraphics/202206A309.html

**2. China’s wildlife trade**:

- MARCH 4, 2020 - https://multimedia.scmp.com/infographics/news/china/article/3064927/wildlife-ban/index.html

- MARCH 5, 2020 - https://multimedia.scmp.com/culture/article/SCMP-printed-graphics-memory/lonelyGraphics/202003A250.html

**3. Godzilla: evolution of a monster**:

- MAY 18, 2014 - https://multimedia.scmp.com/culture/article/SCMP-printed-graphics-memory/lonelyGraphics/201405A83.html

- MAY 29, 2019 - https://multimedia.scmp.com/infographics/culture/article/3012245/godzilla/index.html

**Es importante no confundir las partes con el todo. Recordemos que el análisis de una infografía no es lo mismo que el análisis de una gráfica (sea figurativa, no-figurativa o mixta)**.

Para recuperar el "todo" de las infografías digitales sobre [Bamboo scaffolding in Hong Kong](https://multimedia.scmp.com/infographics/culture/article/3183200/bamboo-scaffolding/index.html), [China’s wildlife trade](https://multimedia.scmp.com/infographics/news/china/article/3064927/wildlife-ban/index.html) y [Godzilla: evolution of a monster](https://multimedia.scmp.com/infographics/culture/article/3012245/godzilla/index.html) deben copiar su URL, ingresar luego a https://www.site-shot.com/ donde pegar la URL copiada, luego activar la opción *full-size*, ajustar *scale* y tomar el pantallazo.

- - - - - - - - 

**Para recuperar las partes que nos interesan en las infografías digitales ya referidas, podemos revisar el código fuente de cada una**.

La manera más sencilla de acceder al código, para hacer esta revisión, es escribir `view-source:` justo antes del `https://…` en la barra de dirección del navegador web (esto funciona en Chrome y Firefox, los navegadores que consideramos como [herramientas del curso](https://github.com/profesorfaco/dno075-2023-1#herramientas)).

Partamos con las **líneas 108 y 109 del código fuente de [Bamboo scaffolding in Hong Kong](https://multimedia.scmp.com/infographics/culture/article/3183200/bamboo-scaffolding/index.html)**, donde podemos encontrar un par de gráficas en SVG cuya dirección completa es:

- https://multimedia.scmp.com/infographics/culture/article/3183200/bamboo-scaffolding/svg/plant-d.svg

- https://multimedia.scmp.com/infographics/culture/article/3183200/bamboo-scaffolding/svg/plant-m.svg

Sigamos en el mismo código fuente, y avancemos a las **líneas 121 y 122**, donde podemos encontrar un segundo par de gráficas en SVG:

- https://multimedia.scmp.com/infographics/culture/article/3183200/bamboo-scaffolding/svg/poles-d.svg

- https://multimedia.scmp.com/infographics/culture/article/3183200/bamboo-scaffolding/svg/poles-m.svg

Cambiemos de infografía. Ahora vamos a **líneas 151 y 152 en el código fuente de [China’s wildlife trade](https://multimedia.scmp.com/infographics/news/china/article/3064927/wildlife-ban/index.html)**, donde podemos encontrar un tercer par: 

- https://multimedia.scmp.com/infographics/news/china/article/3064927/wildlife-ban/svg/pangolin_facts.svg

- https://multimedia.scmp.com/infographics/news/china/article/3064927/wildlife-ban/svg/pangolin_phone.svg

Y en la infografía de **[Godzilla: evolution of a monster](https://multimedia.scmp.com/infographics/culture/article/3012245/godzilla/index.html) revisaremos las líneas 102 y 103** para encontrar este último par encontrar un cuarto par de gráficas en SVG.

- https://multimedia.scmp.com/infographics/culture/article/3012245/godzilla/svg/legendary.svg

- https://multimedia.scmp.com/infographics/culture/article/3012245/godzilla/svg/legendary_m2.svg

- - - - - - - - - -

**Tenemos 4 pares de gráficas que se intercambian. Su intercambio responde al ancho de la pantalla con la que se visualiza la infografía digital de la que son parte**.

Nosotros podemos hacer que estas gráficas se intercambien utilizando [unas clases predefinidas de Bootstrap](https://getbootstrap.com/docs/5.3/utilities/display/) en el `<object></object>` que, como aprendimos la clase recién pasada, puede ser uno de los elemento de HTML más adecuado para tomar y mostrar estos gráficos de formato SVG.

Por ejemplo, copia y pega el siguiente código en un documento nuevo, creado en un editor de código fuente. Guarda tal documento como `ejemplo.html`. Abre este documento en un navegador web y ajusta el tamaño de la pantalla.

```
<!DOCTYPE html>
<html lang="es">
    <head>
        <meta charset="utf-8" />
        <meta name="viewport" content="width=device-width, initial-scale=1" />
        <title>Ejemplo</title>
        <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha2/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-aFq/bzH65dt+w6FI2ooMVUpc+21e0SRygnTpmBvdBgSdnuTN7QbdgL+OapgHtvPp" crossorigin="anonymous" />
    </head>
    <body>
        <div class="container">
            <object data="https://multimedia.scmp.com/infographics/culture/article/3183200/bamboo-scaffolding/svg/poles-d.svg" type="image/svg+xml" class="d-none d-md-block"></object>
            <object data="https://multimedia.scmp.com/infographics/culture/article/3183200/bamboo-scaffolding/svg/poles-m.svg" type="image/svg+xml" class="d-md-none"></object>
        </div>
    </body>
</html>
```

Cuando la ventana del navegador tiene un ancho menor al mediando, que es definido por Boostrap 5 como 768px:

- se despliega `poles-m.svg` (que es traído a esta página por el objeto que tiene la clase `d-md-none`, con un `d-block` tácito) 

- no hay despliegue para `poles-d.svg` (que es traído a esta página por el objeto que tiene la clase `d-none d-md-block`)

Pero cuando la ventana del navegador es igual o mayor al ancho mediano (768px), `poles-d.svg` sí se despliega (por el `d-md-block`). El que ahora no se despliega es `poles-m.svg` (por el `d-md-none`). 

El hecho de que un SVG tenga un nombre que incluya la *d* de *desktop* o la *m* de *mobile*, realmente no afecta en nada al despliegue, porque esto no se resuelve con la denominación del SVG, sino con clases de CSS que se vinculan a un despliegue (*display*); tales letras podrían servir de referencia a humanos que convinieron, para este caso, lo que implicaba una *d* o una *m*.

- - - - - - - - -

Pero eso no es todo lo que examinaremos hoy. Es importante que en cada uno de los 8 SVG podamos examinar el uso del elemento [\<image>](https://developer.mozilla.org/en-US/docs/Web/SVG/Element/image) que permite a cada imagen vectorial incluir otra, sea también vectorial o rasterizada.

Además de hacer tal examen, vamos a tomar cada SVG y traerlo (con lo que incluya cada uno) a una carpeta `img` que vamos a crear dentro de una carpeta que también tiene que contener un [`index.html`](https://profesorfaco.github.io/dno075-2023-1/clase-05/) y un [`style.css`](https://profesorfaco.github.io/dno075-2023-1/clase-05/style.css).

- - - - - - - - -

#### AYUDA

La próxima semana tenemos una evaluación que será individual, por lo que es recomendable que el trabajo de hoy, que adelanta algo de la evaluación, se resuelva individualmente.

Lo recomendable es que cada estudiante use [su cuenta en GitHub](https://github.com/) para:

1. [crear un repositorio](https://docs.github.com/es/get-started/quickstart/create-a-repo) con un nombre identificable (ej: `https://github.com/user/infodigital-clase-05`); y

2. [activar GitHub Pages](https://docs.github.com/es/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site) para poder ver su trabajo en línea, como página web construida con [HTML](https://developer.mozilla.org/es/docs/Learn/HTML/Introduction_to_HTML/Getting_started), a la que cualquiera accede por [HTTP](https://es.wikipedia.org/wiki/Protocolo_de_transferencia_de_hipertexto), después de apuntar a una dirección única ([URL](https://es.wikipedia.org/wiki/Localizador_de_recursos_uniforme)) (ej: `https://user.github.io/infodigital-clase-05`)

- - - - - - - - - - 

###### [← CLASE PASADA](https://github.com/profesorfaco/dno075-2023-1/tree/main/clase-04) — [CLASE SIGUIENTE →](https://github.com/profesorfaco/dno075-2023-1/tree/main/clase-06) 

