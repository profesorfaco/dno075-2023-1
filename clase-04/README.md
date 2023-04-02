# Infografías con SVG

### [Infografía Digital, 6ta. versión](https://github.com/profesorfaco/dno075-2023-1#readme) → Clase 04 → 28/03/2023 ✓

**Ya hemos trabajado con imágenes rasterizadas**, que se describen mediante un conjunto o mapa de bits dentro de una cuadrícula rectangular de píxeles o puntos. Ya conocemos distintos formatos de archivo para este tipo de imágenes: `.GIF`, `.JPG` o `.PNG`. A tales podríamos sumar, más adelante, formatos "next-gen" tales como [`.WebP`](https://www.adobe.com/cl/creativecloud/file-types/image/raster/webp-file.html) o [`.AVIF`](https://es.wikipedia.org/wiki/AVIF).

Ya sabemos que nos conviene cuidar el peso de tales archivos. Este cuidado tiene que apuntar al uso de las dimensiones justas y necesarias para cada caso, además de una compresión más inteligente. Las dimensiones se pueden cuidar con Photoshop o [Photopea.com](https://www.photopea.com/), mientras que la compresión se puede cuidar con la opción de [exportar para web del mismo Photoshop](https://helpx.adobe.com/es/photoshop-elements/using/optimizing-images.html), y/o [tinypng.com](https://tinypng.com/)

**Desde hoy vamos a trabajar con otro tipo de imagen, con imágenes vectoriales**, que se crean mediante la definición de puntos y curvas. Por tal condición se mantienen enfocadas y nítidas, independiente de su tamaño.

**Todas las imágenes vectoriales son escalables, y algunas pueden ser SVG (Scalable Vector Graphics)**. Es muy probable que ya hayamos visto SVG como una extensión con la que es posible guardar un archivo de Adobe Illustator. Menos probable es haber visto:

```
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100">
<path d="M11.25,57c0-17.72,10.21-31.61,18.21-38.5h1.6c-.62.86-4.18,10.7-4.18,20.66,0,9.47,2.46,18.45,6,22.76L45.2,61,31.67,72.72v2.09L51.23,73l19.68,1.84V72.72L57.26,61l13,.86V60.42L57.13,48.61l12.55.86a27.64,27.64,0,0,0,2.71-11.68,33.6,33.6,0,0,0-2.46-11.32h1.23A38.67,38.67,0,0,1,88.75,59.19c0,18.21-15.63,32.1-32.48,35.06V80.35a29.21,29.21,0,0,0-10.08-1.6V94.61C28.23,92.65,11.25,76.66,11.25,57Zm23.5-7.63,10.58-.74L33.89,59.44A44.61,44.61,0,0,1,34.75,49.35ZM51.23,30.16,35.36,45.29c3.08-14.88,10-25.34,10-35a13,13,0,0,0-1-4.55h1.48c10.21,6,23.74,22.63,23.74,32.22A22.67,22.67,0,0,1,68,46.64Z"></path>
</svg>
```

Hagamos un ejercicio con el código que justo arriba pueden ver y copiar. Para este ejercicio necesitamos un editor de código fuente o un block de notas. Vamos a crear un documento nuevo en el editor o el block, y allí pegar el código copiado, para luego guardarlo como `guemil.svg`. Una vez guardado, arrastren el documento a una ventana nueva en su navegador. 

¿Qué es lo que ven en tal ventana? ¿Notan que, independiente del tamaño de la ventana, lo que ven se mantiene enfocado y nítido? 

Lo que ven es una imagen vectorial basada en un único [\<path>](https://developer.mozilla.org/en-US/docs/Web/SVG/Tutorial/Paths), lo que es una entre varias [formas básicas](https://developer.mozilla.org/en-US/docs/Web/SVG/Tutorial/Basic_Shapes) disponibles en este [lenguaje XML, parecido a XHTML, que puede ser usado para dibujar gráficos vectoriales](https://developer.mozilla.org/es/docs/Web/SVG/Tutorial/Introduction).

Si es que tienen instalado Illustrator o Inkscape en sus computadores pueden abrir allí el documento `‌guemil.svg`, para luego editarlo a un modo WYSIWYG (What You See Is What You Get), y luego guardarlo como `guemil_editado.svg`, así podrían comparar sus códigos.

- - - - - - - - - - - - - - - 
  
Llegado a este punto podemos volver a https://app.rawgraphs.io/ y esta vez usar `.svg` como opción de descarga.

Para tener 3 gráficos no figurativos distintos, puedes modificar su nombre agregando un número, por ejemplo: `viz-1.svg`, `viz-2.svg`, `viz-3.svg`.

Para que el resultado sea más legible, podrías meter el código fuente de cada `vis-x.svg`en https://webformatter.com/

También podemos aprovechar más íconos ofrecidos por [Guemil](https://www.guemil.info/icons/), [Noun Project](https://thenounproject.com/icons/), [OpenMoji](https://openmoji.org/library/) y un largo etcétera.

O bien, podemos comenzar a generar nuestras propias imágenes vectoriales en Adobe Illustrator u otra aplicación similares, tales como [Figma](https://www.figma.com/community/plugin/814345141907543603/SVG-Export) o [InkScape](https://inkscape.org/es/)

**Las posibilidades recién mencionadas serán las que utilizaremos para completar [el ejercicio de hoy](https://profesorfaco.github.io/dno075-2023-1/clase-04/)**

#### AYUDA

Tienen que usar el `index.html` en la carpeta de esta clase-04, que pueden ver como [resultado en línea](https://profesorfaco.github.io/dno075-2023-1/clase-04/) (gracias a GitHub Pages) o como [código fuente](https://github.com/profesorfaco/dno075-2023-1/blob/main/clase-04/index.html)

Una persona en la dupla tendrá que usar [su cuenta en GitHub](https://github.com/) para:

1. [crear un repositorio](https://docs.github.com/es/get-started/quickstart/create-a-repo) con un nombre identificable (ej: `https://github.com/user/infodigital-clase-04`); y

2. [activar GitHub Pages](https://docs.github.com/es/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site) para poder ver su trabajo en línea, como página web construida con [HTML](https://developer.mozilla.org/es/docs/Learn/HTML/Introduction_to_HTML/Getting_started), a la que cualquiera accede por [HTTP](https://es.wikipedia.org/wiki/Protocolo_de_transferencia_de_hipertexto), después de apuntar a una dirección única ([URL](https://es.wikipedia.org/wiki/Localizador_de_recursos_uniforme)) (ej: `https://user.github.io/infodigital-clase-04`)

#### VÍNCULOS EN EL [FORO DE DISCUSIÓN](https://cursos.canvas.uc.cl/courses/56995/discussion_topics/583157)

|	N°	|	Nombres	|	GitHub Page	|
|:------:|:------------------------|:------------------|
|	1	|	CONSTANZA	ALVARADO	|	—	|
|	2	|	AGUSTÍN	AVENDAÑO	|	—	|
|	3	|	DANIEL	CARMONA	|	https://tomsbinary.github.io/clase4/	|
|	4	|	CELESTE	CASTILLO	|	—	|
|	5	|	EMMET	CHAVEZ	|	https://palomanapo.github.io/Clase_cuatro/	|
|	6	|	VICENTE	DE VIDTS	|	https://tomsbinary.github.io/clase4/	|
|	7	|	CLARA	ECHEVERRÍA	|	https://claraecheverria1.github.io/clase4.info/	|
|	8	|	MARÍA JOSEFA	GARCÍA	|	—	|
|	9	|	YANNLING	KUO	|	https://yannlingk.github.io/infodigital-clase-04/	|
|	10	|	ROSARIO	MORALES	|	https://antooot.github.io/clase-04/	|
|	11	|	ANTONIA	MORENO	|	https://antoniamoreno.github.io/clase-04/	|
|	12	|	PALOMA	NAVARRETE	|	https://palomanapo.github.io/Clase_cuatro/	|
|	13	|	MAGDALENA	PINO	|	https://magdapino.github.io/cuarta-clase/	|
|	14	|	KATIA	QUINTANILLA	|	—	|
|	15	|	CRISTÓBAL	QUIROZ	|	—	|
|	16	|	MAXIMILIANO	RAMÍREZ	|	https://maxramirezolea.github.io/4_Clase/	|
|	17	|	ANTONIA	TAPIA	|	https://antooot.github.io/clase-04/	|
|	18	|	FLORENCIA	VALDIVIESO	|	—	|
|	19	|	EMILIA	VERGARA	|	https://yannlingk.github.io/infodigital-clase-04/	|
|	20	|	MARÍA VICTORIA	VIAL	|	—	|

- - - - - - - 

###### [← CLASE PASADA](https://github.com/profesorfaco/dno075-2023-1/tree/main/clase-03) — [CLASE SIGUIENTE →](https://github.com/profesorfaco/dno075-2023-1/tree/main/clase-05) 
