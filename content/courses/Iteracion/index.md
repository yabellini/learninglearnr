---
date: "2021-04-17T00:00:00Z"
external_link: ""
image:
  caption:  Isabella and Zsa Fischer en Unsplash
  focal_point: Smart
links:
- icon: twitter
  icon_pack: fab
  name: Follow
  url: https://twitter.com/yabellini
slides: 
summary: Paquete con dos tutoriales para aprender Iteración en R
tags:
- Tutorial
- purrr

title: Tutorial de introducción a la iteracción con R
url_code: https://github.com/yabellini/TutorialIterar
url_pdf: ""
url_slides: ""
url_video: ""
---

El objetivo de este paquete contiene dos tutoriales para introducir el concepto de iteración en R.

La iteración es la tarea de aplicar una función de forma iterativa a cada elemento de un vector. El primer tutorial explicará qué es un vector e introducirá dos formas de iterar en R: bucles `for` y el paquete `purrr`.

El segundo tutorial introduce la familia de funciones map de `purrr` que hace que la iteración sea rápida y fácil. Aprenderás los secretos de `map()` y sus variantes.

Si quieren colaborar [aquí está el repo](https://github.com/yabellini/tutorialgRaficosFN)


Para instalar la versión de desarrollo desde GitHub, escribe el siguiente código (tal vez debas intalar el paquete `remotes` con `install.packages("remotes")`):

`remotes::install_github("yabellini/TutorialIterar")`

Si se intaló correctamente y tienes la última versión de RStudio aparecerá en tu panel de **Tutorial**.

Si no tienes la ultima versión entonces hay que instalar el paquete [learnr](https://rstudio.github.io/learnr/index.html) con `install.packages("learnr")` y luego ejecutar los tutoriales de esta manera:

* Tutorial Primeros pasos para iterar con R:

`learnr::run_tutorial("PrimerosPasos", package = "TutorialIterar")`

* Tutorial Introducción a las funciones Map :

`learnr::run_tutorial("IntroFuncionesMap", package = "TutorialIterar")`

Espero que les sirva, se diviertan y aprendan