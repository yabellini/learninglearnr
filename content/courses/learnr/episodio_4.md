---
date: "2020-10-03T00:00:00Z"
draft: false
lastmod: "2020-10-03T00:00:00Z"
linktitle: Generando tutoriales interactivos con el paquete {learnr}
menu:
  learnr:
    name: Episodio 4
    weight: 6
summary: Aprende como usar {learnr} para construir tutoriales interactivos con R.
title: Episodio 4
toc: true
type: docs
weight: 6
---

## Publicando el tutorial

### Compartiendo el tutorial

Los tutoriales se pueden publicar de la misma manera que las aplicaciones Shiny, incluyendo la ejecución local en la máquina de un usuario final, en un servidor Shiny o un servicio de alojamiento como shinyapps.io.  Para esta última opción se puede utilizar el botón de _Publish Document_ presente en la IDE de RStudio.

También existe la posibilidad de publicarlo utilizando `binder`, para más información sobre esta opción recomendamos [este artículo](http://laderast.github.io/2020/09/15/getting-learnr-tutorials-to-run-on-mybinder-org/) de _Ted Laderas_(en inglés).

Otra forma de implementar un tutorial es incluirlo dentro de un paquete R y hacer que los usuarios lo ejecuten directamente a través de la función `learnr::run_tutorial`. Para más información sobre como realizar esta tarea pueden consultar [el siguiente post](https://education.rstudio.com/blog/2020/09/delivering-learnr-tutorials-in-a-package/) de RStudio Education (en inglés).

## Ejercicio: 10 minutos

* Sobre el tutorial que crearon en el ejercicio anterior:
* Publicarlo en https://www.shinyapps.io/ utilizando la IDE de RStudio (es necesario tener una cuenta en shinyapps.io)
