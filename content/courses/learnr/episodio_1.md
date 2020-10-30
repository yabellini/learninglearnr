---
date: "2020-10-03T00:00:00Z"
draft: false
lastmod: "2020-10-03T00:00:00Z"
linktitle: Generando tutoriales interactivos con el paquete {learnr}
menu:
  learnr:
    name: Episodio 1
    weight: 4
summary: Aprende como usar {learnr} para construir tutoriales interactivos con R.
title: Episodio 1
toc: true
type: docs
weight: 4 
---

Nuestro objetivo en este curso es introducirnos en el mundo de los tutoriales interactivos generados con el paquete `learnr`.  

{{< figure src="/media/recursos.png" alt="pantallas de ejemplo de tutoriales contruidos utilizando learnr">}}

¿Qué son estos tutoriales interactivos?, vamos a analizar unos ejemplos para ver de que hablamos:

* Tutorial donde se introduce el tema de [valores faltantes](https://allisonhorst.shinyapps.io/missingexplorer/) y como trabajarlos realizado por _Allison Horst_.

* [Jirafas Tacitas de Té](https://tinystats.github.io/teacups-giraffes-and-statistics/01_introToR.html) de _Desirée De Leon_.

* Tutoriales de [RStudio primers](https://rstudio.cloud/learn/primers) que introducen conceptos de Ciencia de Datos con R.

* Tutorial de _Lisa Lendway_ para su clase [COMP/STAT 112: Introduction to Data Science](https://github.com/llendway/DS112tutorials) en Macalester College.

Hay muchos más ejemplos para ver, pero estos cuatro presentan diferentes características con respecto a la forma de publicación: el primero se publica como una aplicación Shiny, el segundo utiliza `learnr` embebido en un sitio generado con blogdown (por detrás son aplicaciones shiny), el tercer ejemplo está publicado en RStudio Cloud y el último se pone a disposición como un paquete.

Además creemos que también son una muestra interesante de las posibilidades de personalización de los tutoriales en cuanto a la identidad visual (colores, tipos de fuentes, etc.).

## Entonces: ¿pará qué pueden ser útiles los tutoriales interactivos?

* Enseñanza remota:

  * 

* Enseñanza presencial:

  * _Aula invertida_: se puede generar tutoriales interactivos con explicaciones y ejemplos implementados en R sobre una serie de conceptos nuevos, para que los y las estudiantes puedan practicarlos antes de tener la clase.  Luego se explican estos conceptos en clase utilizando menos tiempo y ese tiempo extra dedicarlo a realizar ejercicios prácticos durante la clase (que pueden ser también un tutorial `learnr`).
  
  * _Seguimiento_: proveer el tutorial interactivo con el mismo contenido de la clase como estratégia de seguimiento del curso.  Esto también aplica a talleres o cursos cortos, donde el tutorial interactivo puede ser parte del material que se provee a los asistentes y permite tener un alcance que va más allá del tiempo del curso o taller.
  
  * _Ejercicios_: tanto sea la práctica en clase/laboratorio o como tarea a resolver.

* Auto aprendizaje: si publicamos nuestros tutoriales, más personas podrán utilizarlos para aprender.  Especialmente se puede aplicar el concepto de aprender haciendo, que funciona mucho mejor que métodos más pasivos, como por ejemplo sólo escuchar a un video o una clase.

* Desarrollo de paquetes: se pueden integrar tutoriales interactivos como parte de un paquete, por lo que se puede proveer a los posibles usuarios del paquete una forma más rica de aprender que la pagina de ayuda y/o las viñetas.


 
  

* 