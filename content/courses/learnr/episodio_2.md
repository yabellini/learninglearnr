---
date: "2020-10-03T00:00:00Z"
draft: false
lastmod: "2020-10-03T00:00:00Z"
linktitle: Generando tutoriales interactivos con el paquete {learnr}
menu:
  learnr:
    name: Episodio 2
    weight: 5
summary: Aprende como usar {learnr} para construir tutoriales interactivos con R.
title: Episodio 2
toc: true
type: docs
weight: 5
---

## Preguntas en {learnr} 

Se pueden incluir una o más preguntas de opción múltiple dentro de un tutorial para verificar que los estudiantes entendieron los conceptos presentados. Las preguntas pueden tener una o múltiples respuestas correctas. Para incluirlas se debe llamar a la función `question` o `quiz` dentro de un chunk de R de esta manera:

````
```{r quiz}
quiz(
  question("¿Qué paquete del listado nos permite realizar gráficos?", 
  correct = "Buen trabajo!, ggplot2 es el paquete que nos permite realizar gráficos.", 
  allow_retry = TRUE,
    answer("ggplot", message = "Cerca, pero no...intentalo de nuevo!"),
    answer("gplot2", message = "Nop...intentalo de nuevo!"),
    answer("plot2", message = "Incorrect. Intenta de nuevo!."),
    answer("ggplot2", correct = TRUE)
  ), caption = "Visualización"
)
```
```` 
La pregunta se presenta dentro de una “cajita” con el botón _Submit Answer_ (enviar respuesta), en caso que la respuesta sea correcta, debajo de la pregunta aparece un recuadro verde con el mensaje estipulado en el atributo `correct` de la función `question`. 

En caso de que la respuesta sea incorrecta aparece un recuadro rojo, con el texto indicado en el atributto `message` de la función `answer` y un botón _Try again_ (intenta de nuevo), gracias al atributo `allow_retry = TRUE`. 
Se pueden poner esos botones con otro mensaje y en español utilizando la función `question` y los parámetros: `submit_button = "Enviar respuesta"` y `try_again_button = "Intenta de nuevo"`.

En la figura se detalla el código y como se visualiza cada opción en la interfaz del tutorial con dos preguntas de ejemplo: una con opciones excluyentes y otra con más de una opción correcta.

{{< figure src="/media/learner_partes_de_una_pregunta.png" alt="preguntas multiple choise en learnr">}}

## Ejercicio: 10 minutos!!!

* Sobre el tutorial que crearon en el ejercicio anterior:
* Vayan hasta las preguntas (### Quiz) y modifiquen:
  - la primera pregunta para que tenga un mensaje cuando la opción es incorrecta y permita intentarlo de nuevo.
  - La segunda pregunta para que se pueda intentarlo de nuevo y muestre un mensaje de “Muy bien!” cuando se seleccionan las respuestas correctas.
* Consulten la ayuda para `?question` y `?quiz` (o presionando F1 arriba del nombre de la función) .

