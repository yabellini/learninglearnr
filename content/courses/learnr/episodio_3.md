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

En los tutoriales un chunk de código puede transformarse en un **ejercicio**.  Los ejercicios presentarán al estudiante un espacio para escribir código, ejecutarlo y recibir una respuesta.  Este espacio puede estar *vacio* o puede *tener código previo incompleto*, para que el estudiante lo complete con la solución correcta.  Además hay ejercicios que pueden *presentar pistas y/o la solución*.

### Ejercicio vacio

Para generar un ejercicio simple, sin código, se agrega el parámetro `exercice = TRUE` al chunk de R: 

````
```{r dos-mas-dos, exercise=TRUE}

```
```` 

Cuando compilamos el documento en el lugar del chunk de ejercicio se presenta una "caja" donde se puede escribir código y el botón `Run Code` (ejecutar código), presionándolo, se ejecuta el código escrito presentando el resultado correspondiente (sea una salida o un mensaje).

### Ejercicio con código previo, consejos y solución

Los chunks de ejercicios pueden contener código para completar, como una plantilla, para ayudar al estudiante a resolver la ejercitación o para concentrarse sólo en el tema o característica que estamos enseñando.


````markdown
```{r funcion-sumar, exercise=TRUE, exercise.lines = 5}
sumar <- function(___,___) {
  ______
}

sumar(___,___)
```
````

{{< figure src="/media/ejercicio_con_consejo_learnr.png" alt="Ejemplos de código para completar, pista y consejo y como se ve en el tutorial">}}


Si se quiere dar algunas pistas para ayudar a los estudiantes en la resolución de los ejercicios, especialmente si conocemos que el tema que estamos enseñando tiene errores de compresión comunes, podemos hacerlo generando un nuevo chunk de R con el mismo nombre que el chunk del ejercicio al que le agregamos la palabra `-hint`.

````markdown
```{r funcion-sumar-hint}
sumar <- function(___,___) {
  # Aqui debe ir el calculo sumando los dos parámetros 
  # que debe tener la función para recibir los dos números a sumar
}

sumar(___,___)
```
````

También podemos proveer la solución esperada, especialmente porque los problemas de programación pueden tener más de una solución válida.  Para ello generamos un nuevo chunk de R, con el mismo nombre del ejercicio y le agregamos la palabra `-solution`.

````markdown
```{r funcion-sumar-solution}
sumar <- function(numero1,numero2) {
  numero1+numero2
}

sumar(5,3)
```
````

{{< figure src="/media/consejos_y_soluciones_learnr.png" alt="Ejemplos de código para con consejo(pista) y solución y como se ve en el tutorial">}}


Cuando escriban estos chunks en RStudio, se van a marcar errores en las secciones donde el código está incompleto, esto se ignora cuando se compila el documento gracias al atributo `exercice=TRUE` del primer chunk.


### Ejercicio: 10 minutos!!! 

* Sobre el tutorial que crearon en el ejercicio anterior:
* Revisen los ejercicios propuestos y modifiquen:
  - El primer ejercicio para que incluya una pista (hint) y la solución (solution).
  - El segundo ejercicio para que  incluya código y secciones a completar.
* Recuerden compilar el documento para ver los cambios y el funcionamiento de la solución.





Se pueden incluir una o más preguntas de opción múltiple dentro de un tutorial para verificar que los estudiantes entendieron los conceptos presentados. Las preguntas pueden tener una o múltiples respuestas correctas. Para incluirlas se debe llamar a la función question o quiz dentro de un chunk de R de esta manera:

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

