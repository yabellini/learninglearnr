---
date: "2020-01-08"
draft: false
type: page
linktitle: Recursos para explorar y aprender learnr
summary: en este post listo una serie de recursos para seguir aprendiendo learnr.
title: Recursos para explorar y aprender learnr
authors: 
    - yabellini
type: post
weight: 1
tags: 
    - Recursos
---

{{< figure src="/media/recursos.svg" alt="Captura de pantallas de diferentes tutoriales learnr">}}

En este post les comparto mi lista de materiales que me ayudaron a aprender sobre `learnr`.  Este listado se va actualizando en [este repositorio](https://github.com/yabellini/curso_learnr).


## Otros tutoriales

Los tutoriales construidos por otras personas fue uno de los primeros recursos que exploré para ver como y para qué se usaban estos tutoriales, van aquí mis favoritos.  Además comparten el código fuente y por ende podemos aprender como están hechas cada una de las herramientas que se usan en el tutorial.

* [RStudio Primers](https://rstudio.cloud/learn/primers): son una serie de tutoriales de RStudio generados para aprender conceptos básicos de ciencia de datos con los tutoriales interactivos.  Se agrupan en seis temas: conceptos básicos, trabajando con datos, visualizando datos, ordenando tus datos, iterando y escribiendo funciones.  Desde [este repositorio de github](https://github.com/rstudio-education/primers) se puede acceder a su código fuente.

* [Data Science in a box](https://datasciencebox.org/interactive-tutorials.html): serie de tutoriales del conocido curso de Mine Çetinkaya-Rundel.  Presenta 8 tutoriales que se pueden usar desde Shiny, instalarse como paquete y acceder a su código fuente. Los he ustilizado para aprender como usar el paquete `gradethis` junto con `learnr` para evaluar ejercicios de forma automática.


## Paquetes para usar con `learnr`

Hay paquetes que nos pueden ayudar a agregarle funcionalidades a nuestros tutoriales.

* [Gradethis](https://rstudio-education.github.io/gradethis/)

* [Parsons](https://github.com/rstudio/parsons)

* [Sortable](https://github.com/rstudio/sortable)

* [glosario](https://github.com/carpentries/glosario-r)

* [Flash Cards](https://github.com/henningsway/r2anki) y (https://github.com/jienagu/flashCard)

## Charlas

## Cursos y workshops

## Blogpost

Este listado de blog post presentan de forma clara, paso a paso y ejemplos funcionales de diferentes partes del desarrollo de un tutorial de `learnr`, la mayoría están en Inglés.

### Utilizando learnr con gradethis

* [Data science tutorials with learnr and gradethis](http://www.citizen-statistician.org/2020/08/data-science-tutorials-with-learnr-and-gradethis/) por Lee Suddaby, Zeno Kujawa 

### Publicando tutoriales:

* [Delivering learnr tutorials in a package](https://education.rstudio.com/blog/2020/09/delivering-learnr-tutorials-in-a-package/) por Desirée De Leon

* [Getting a learnr tutorials to run on mybinder.org](http://laderast.github.io/2020/09/15/getting-learnr-tutorials-to-run-on-mybinder-org/) por Ted Laderas

* [Publishing learnr Tutorials on shinyapps.io](https://cran.r-project.org/web/packages/learnr/vignettes/shinyapps-publishing.html) por Angela Li