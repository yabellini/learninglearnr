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

title: Tutorial: Intro a ggplot2 para 30 días de gráficos
url_code: https://github.com/yabellini/tutorialgRaficosFN
url_pdf: ""
url_slides: ""
url_video: ""
---

El 12 de mayo empezó #30díasdegráficos con R, una iniciativa de la comunidad hispanohablante de R para recordar a __Florence Nightingale__ y aprender sobre visualización de datos.  

El desafío: crear y compartir un gráfico al día.  Más info sobre la iniciativa [aquí](https://github.com/cienciadedatos/datos-de-miercoles/blob/master/30-dias-de-graficos-2020.md)

Como no pude participar haciendo los gráficos para cada día, generé este *mini tutorial* usado el paquete `learnr` donde explico como hacer una serie de gráficos con `ggplot2`.  Con el tiempo, prometo ir mejorando el contenido y agregando cómo generar más tipos de gráficos.  

Si quieren colaborar [aquí está el repo](https://github.com/yabellini/tutorialgRaficosFN)

Mis objetivos al generar este tutorial fueron:

 * aprender a generar un paquete de un tutorial desarrollado en `learnr`. Usé el material del tutorial [“Package Development"](https://github.com/hadley/pkg-dev) que Hadley Wickham dictó en LatinR 2019.
 * incluir en el tutorial una serie de herramientas pedagogicas descriptas en el libro [Teaching Tech Together](https://teachtogether.tech/es/index.html)
 * aprovechar el nuevo panel de Tutorial que viene en la [nueva versión de RStudio](https://rstudio.com/products/rstudio/download/preview/).
 * aprender como cambiar los estilos del tutorial basado [este post](https://education.rstudio.com/blog/2020/05/learnr-for-remote/)
 * hacer un aporte al festejo de **Florence Nightingale** 

Por eso el tutorial incluye un [mapa conceptual](/post/concept_maps.md) con los temas que cubre, dos [learner personas](/post/learner_personas.md) en las cuales pensé mientras lo contruí, la [licencia de uso](), una serie de explicaciones y ejercicios para hacer gráficos en R y las fuentes de consulta.

Para instalar la versión de desarrollo desde GitHub, escribe el siguiente código (tal vez debas intalar el paquete `remotes` con `install.packages("remotes")`):

`remotes::install_github("yabellini/tutorialgRaficosFN")`

Si se intaló correctamente y tienes la última versión de RStudio aparecerá en tu panel de **Tutorial**.

Si no tienes la ultima versión entonces hay que instalar el paquete [learnr](https://rstudio.github.io/learnr/index.html) con `install.packages("learnr")` y luego ejecutar el tutorial de esta manera:

`learnr::run_tutorial("graficos", package = "TutorialgRaficosFN")`

Así se ve el tutorial cuando está ejecutandose:

 {{< figure src="/media/learnr_contenido_ggplot.png" alt="Ejemplo del contenido del tutorial">}}

Espero que les sirva y se diviertan....definitivamente yo lo hice mientras lo construí.