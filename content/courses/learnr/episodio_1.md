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

* Enseñanza remota: el año 2020 trajo consigo al COVID-19 que implicó que las clases presenciales fueran suspendidas y tengan que ser dictadas en forma remota.  Los tutoriales de `learnr`pueden ayudar:

  * Evitando la necesidad de una computadora o concimientos avanzados para instalar el software necesario para programar, si se publica como una aplicación Shiny (aunque esta opción puede traer problemas en los costos de algunos servicios de publicación de aplicaciones)
  
  * Dando feedback inmediato a la resolución de problemas (por medio de preguntas y ejercicios)  

* Enseñanza presencial:

  * _Aula invertida_: se puede generar tutoriales interactivos con explicaciones y ejemplos implementados en R sobre una serie de conceptos nuevos, para que los y las estudiantes puedan practicarlos antes de tener la clase.  Luego se explican estos conceptos en clase utilizando menos tiempo y ese tiempo extra dedicarlo a realizar ejercicios prácticos durante la clase (que pueden ser también un tutorial `learnr`).
  
  * _Seguimiento_: proveer el tutorial interactivo con el mismo contenido de la clase como estratégia de seguimiento del curso.  Esto también aplica a talleres o cursos cortos, donde el tutorial interactivo puede ser parte del material que se provee a los asistentes y permite tener un alcance que va más allá del tiempo del curso o taller.
  
  * _Ejercicios_: tanto sea la práctica en clase/laboratorio o como tarea a resolver.

* Auto aprendizaje: si publicamos nuestros tutoriales, más personas podrán utilizarlos para aprender.  Especialmente se puede aplicar el concepto de aprender haciendo, que funciona mucho mejor que métodos más pasivos, como por ejemplo sólo escuchar a un video o una clase.

* Desarrollo de paquetes: se pueden integrar tutoriales interactivos como parte de un paquete, por lo que se puede proveer a los posibles usuarios del paquete una forma más rica de aprender que la pagina de ayuda y/o las viñetas.


## ¿Cómo se ve eso en un tutorial?

un tutorial de `learnr` tiene una serie de elementos comunes:

* una tabla de contenidos, sobre la cual se va generando una barra de progreso a medida que el/la estudiante avanza en la lectura y ejecución del tutorial.

* un texto explicando los conceptos o ejercicios a trabajar.

* ejercicios de código que los y las estudiantes pueden ejecutar en el momento y recibir un comentario.

* preguntas de opción múltiple

* otros tipos de contenido como videos, figuras y tablas.
 
 {{< figure src="/media/learner_tutorial.png" alt="se marca en una captura de pantalla las partes de un tutorial de learnr: la barra de progreso arriba a la izquierda, la tabla de contenidos arriba a la izquierda, la narrativa al centro, un ejercicio de código al centro después del texto de la narrativa, una pregunta de opción múltiple luego del ejercicio de código">}}
 

## En el fondo todo es RMarkdown

Una de las ideas más poderosas de `learnr` es poder usar `rmarkdown` para generar estos tutoriales:

{{< figure src="/media/learnr_rmarkdown_episodio1.png" alt="imagen comparando el YAML, los chunk de código y el texto de un documento rmarkdown común y un tutorial learnr">}}

Como se aprecia en la figura el encabezado YAML tiene algunas diferencias con el encabezado de un documento `rmarkdown` común:

```
---
title: "Título del tutorial"
author: Yanina Bellini Saibene (MetaDocencia)
output: 
  learnr::tutorial: #indica que es un tipo tutorial learnr
    css: css/learnr_metadocencia.css #aplica los estilos, si no está usa el standar de learnr
    progressive: true # los encabezados de tercer nivel (###) son revelados progresivamente 
    allow_skip: true # permite saltearse los ejercicios. 
description: "Mi super genial tutorial de R" # Esta descripción se ve en el panel Tutorial de RStudio 
runtime: shiny_prerendered
---
```

Lugo el texto y la manera de darle formato es igual a la que estamos acostumbrados.  Solo debemos saber que los encabezados de segundo nivel (dos numerales ##) son los que se utilizan para armar la tabla de contenido y que los de tercer nivel (tres numerales ###) aparecerán de forma progresiva en caso que así esté específicado en el YAML.

Los chunks de código también se comportan de la misma manera, con excepción de un chunk especial del tipo ejercicio (que veremos en más detalle en el Episodio 3).


{{< figure src="/media/learnr_rmarkdown_diferencias_episodio1.png" alt="imagen comparando el YAML, los chunk de código y el botón de knir convertido en Run Document en la IDE de RStudio">}}

## ¿Cómo genero un nuevo tutorial de learnr?

Primero hay que intalar el paquete {learnr} (`install.packages("learnr")`) y luego de eso seleccionamos **File -> New File -> Rmarkdown -> From Template -> learnr**

Nos presentará una plantilla con los elementos básicos de un tutorial.  


## Ejercicio: 10 minutos


* Generar un nuevo tutorial learnr.
* Corran el documento para ver el aspecto de la plantilla.
* Modifiquen el YAML para que:
  - Agregue una descripción.
  - Avance los temas de forma progresiva.
  - Permita saltear los ejercicios y preguntas sin resolverlas.
* Corran nuevamente el documento para ver esos cambios.
