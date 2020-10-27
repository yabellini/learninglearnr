---
date: "2020-05-21T00:00:00Z"
external_link: ""
image:
  caption: Foto de rawpixel on Unsplash
  focal_point: Smart
links:
- icon: twitter
  icon_pack: fab
  name: Follow
  url: https://twitter.com/yabellini
slides: 
summary: Mini tutorial para generar gráficos en R festejando a Florence Nightingale
tags:
- Tutorial
- ggplot

title: Tutorial 30 días de gráficos
url_code: https://github.com/yabellini/tutorialgRaficosFN
url_pdf: ""
url_slides: ""
url_video: ""
---

El 12 de mayo empezó #30díasdegráficos con R, una iniciativa de la comunidad hispanohablante de R para recordar a Florence Nightingale y aprender sobre visualización de datos.  

El desafío: crear y compartir un gráfico al día.  Más info sobre la iniciativa  [aquí](https://github.com/cienciadedatos/datos-de-miercoles/blob/master/30-dias-de-graficos-2020.md)

Como no pude participar haciendo los gráficos para cada día, generé este *mini tutorial* usado el paquete `learnr` donde explico como hacer una serie de gráficos con `ggplot2`.  Si les gusta prometo ir mejorandolo y agregandole cómo generar diferentes tipos de gráficos.  

Si quieren colaborar [aquí está el repo](https://github.com/yabellini/tutorialgRaficosFN)

Mis objetivos para generar este tutorial fueron:

 * aprender a generar un paquete de un tutorial desarrollado en `learnr`. Usé el material del tutorial [“Package Development"](https://github.com/hadley/pkg-dev) que Hadley Wickham dictó en LatinR 2019.
 * que el tutorial incluya una serie de herramientas pedagogicas descriptas en el libro [Teaching Tech Together](teachtogether.tech/)
 * que pudiera aprovechar el nuevo panel de Tutorial que viene en la [nueva versión de RStudio](https://rstudio.com/products/rstudio/download/preview/).
 * aprender como cambiar los estilos del tutorial basado [este post](https://education.rstudio.com/blog/2020/05/learnr-for-remote/)
 * que hiciera un aporte al festejo de **Florence Nightingale** 

Por eso el tutorial incluye un [mapa conceptual](/post/concept_maps.md) con los temas que cubre, dos [learner personas](/post/learner_personas.md) que son en quienes pensé cuando lo armé, la [licencia de uso](), una serie de explicaciones y ejercicios para hacer gráficos en R y las fuentes de consulta.

Para instalar el paquete tenés que descargarte el archivo [.tar.gz](https://github.com/yabellini/tutorialgRaficosFN/blob/master/TutorialgRaficosFN_0.1.0.tar.gz) o [.zip (este sólo funciona en Windows)](https://github.com/yabellini/tutorialgRaficosFN/blob/master/TutorialgRaficosFN_0.1.0.zip) e instalar el paquete `tutorialgRaficosFN` desde la opción **Tools -> Install Packages -> Install from -> Package Archive File (.zip; .tar.gz)**. Si tenes la última versión de RStudio aparecerá en tu panel de **Tutorial**.

Si no tenes la ultima versión entonces tenés que instalar el paquete [learnr](https://rstudio.github.io/learnr/index.html) y luego ejecutar de esta manera el Tutorial:

`learnr::run_tutorial("graficos", package = "TutorialgRaficosFN")`

Así se ve el tutorial cuando está ejecutandose:

 {{< figure src="/media/learnr_contenido_ggplot.png" alt="Ejemplo del contenido del tutorial">}}

Espero que les sirva/divierta....yo me divertí y aprendí mucho armandoló.