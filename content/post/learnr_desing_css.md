---
date: "2020-11-24"
draft: false
type: page
linktitle: Cambiando el diseño visual de los tutoriales
summary: un ejemplo de una plantilla CSS explicando como cambiar fuentes y colores de los elementos de un tutorial .
title: Cambiando el diseño visual de los tutoriales
authors: 
    - yabellini
type: post
weight: 1
tags: 
    - Recursos
    - tips técnicos
---

## Personalizando nuestros tutoriales

Los tutoriales generados con learnr terminan generando un archivo HTML (siglas en inglés de _Hiper Text Markup Language_), por lo que podemos cambiar su estilo utilizando _CSS_ (siglas en inglés de _Cascading Style Sheets_), en español _Hojas de estilo en cascada_.

CSS está diseñado para separar el contenido del formato de presentación en un documento HTML. El formato de presentación incluye, entre otros elementos, los botones, los menús, las tablas y permite configurar aspectos como que fuente, color y tamaño tendrá cada elemento.  En la figura vemos el estilo por defecto con el que cuentan los tutoriales de `learnr`.

{{< figure src="/media/css_default.png" alt="Elementos de un tutorial learnr y su estilo por defecto">}}

Creando un archivo `.css` podemos personalizar todos los elementos de nuestro tutorial.

## Los elementos de un CSS

Para aprender más sobre CSS y como escribir estas hojas de estilos el siguiente sitio web me fue muy útil. [Acceder al sitio web](https://www.w3schools.com/css)

### Elementos principales

El siguiente código define la fuente y el tamaño de la letra para el cuerpo (`body`) del tutorial.  El tamaño está de acuerdo a las sugerencias de accesibilidad realizadas por MetaDocencia. [Acceder al post](https://www.metadocencia.org/post/accesibilidad_1/)


```{css, eval=FALSE}
body {
  font-family: Arial, Helvetica, sans-serif;
  font-size: 14;
}

```

Los siguientes elementos configuran los títulos, `h1` es el título, es el encabezado que en rmarkdown configuramos con un numeral (#), `h2` corresponde a un subtítulo (dos numerales) y así hasta el encabezado de quinto nivel (`h5`).  En el caso de `h1` y `h2` definimos un color para la fuente (`color`), un color de fondo (`background-color`) y un espacio alrededor del título (`padding`). 

```{css, eval=FALSE}

h1, h2 {
  color: #C83737;
  background-color: #f7f7f7;
  padding: .5em;
}

h3, h4, h5{
  color: #C83737;
}

```
Asi se ven los cambios que realiza este css en la plantilla.  Cambia el color y tamaños del texto de la fuente y del fondo de los encabezados y del título:

{{< figure src="/media/css_cambios_body_encabezados.png" alt="Elementos de un tutorial learnr y su estilo en títulos y encabezados cambiado">}}

Este código configura la apariencia de los links (chequear el .ace-tm).

```{css, eval=FALbasadoSE}
a {
    color: #C83737;
    text-decoration: none;
}

.ace-tm {
    background-color: #ffffff;
    color: black;
}

```

### Botones

Los tutoriales presentan varios botones, por ejemplo: `Continue` que separa los temas; `Submit Answer` y `Try Again` en las preguntas; `Run Code` y `Hints` en los ejercicios.

Para cambiar su apariencia es necesario especificar las propiedades de los botones en general y luego de acuerdo al estado y acciones sobre esos botones (`.btn:hover, .btn:active, .btn:disabled`), como se muestra en el siguiente código:

```{css, eval=FALSE}

.btn {
  background-color: #C83737;
  color: #fff;
}

.btn-default {
    color: #ffffff;
    background-color: #C83737;
    border: none;
}

.btn-light {
  background-color: #aa2f2f;
  color: #fff;
}

.btn-primary , .btn-success, .btn-info{
  background-color: #C83737;
  color: #fff;
}

.btn:hover, .btn:active, .btn:disabled {
  background-color: #aa2f2f;
  color: #fff;
}

```

### Agregar una imágen

{{< figure src="/media/rmarkdown_concept_map.svg" alt="Mapa conceptual de RMarkdown">}}
