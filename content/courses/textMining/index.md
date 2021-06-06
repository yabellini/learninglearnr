---
date: "2021-06-05T00:00:00Z"
external_link: ""
image:
  caption:  Photo by <a href="https://unsplash.com/@borodinanadi?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">nadi borodina</a> on <a href="https://unsplash.com/s/photos/text?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Unsplash</a>
  focal_point: Smart
links:
- icon: twitter
  icon_pack: fab
  name: Follow
  url: https://twitter.com/yabellini
slides: 
summary: Paquete con un tutoriales interactivo de intruducción a la Minería de Texto
tags:
- Tutorial
- Text Mining
- Minería de Texto

title: Tutorial interactivo sobre Minería de Texto
url_code: https://github.com/yabellini/TextMiningTutorial
url_pdf: ""
url_slides: ""
url_video: ""
---

El objetivo de este tutorial interactivo es introducir los conceptos básicos de la minería de texto con un enfoque _tidy_ basado en el libro _Tidy Text_ de Silge y Robinson. 

El tutorial se presenta como un paquete.  Si quieren colaborar [aquí está el repo](https://github.com/yabellini/TextMiningTutorial)


Para instalar la versión de desarrollo desde GitHub tenés que tener instalado el paquete _remotes_, si no lo tenés instalalo con:

``` r
install.packages("remotes")

```
y luego usá el siguiente código para instalar el tutorial:

``` r
remotes::install_github("yabellini/TextMiningTutorial")
```
Puede ser que si hay versiones más nuevas de los paquetes que necesitas en la consola te aparezca un mensaje similar a este:


``` r
These packages have more recent versions available.
It is recommended to update all of them.
Which would you like to update?

 1: All                                 
 2: CRAN packages only                  
 3: None                                
 4: colorspace (1.4-1  -> 2.0-1 ) [CRAN]
 5: rlang      (0.4.2  -> 0.4.11) [CRAN]
 6: glue       (1.4.0  -> 1.4.2 ) [CRAN]
 
 Enter one or more numbers, or an empty line to skip updates:

``` 
Ese mensaje nos indica que paquetes podríamos actualizar. Si no queremos actualizar podemos presionar `Enter` o bien seleccionar el número que dice _None_, en este caso el 3. 

Si no tenes la ultima versión de RStudio entonces tenés que instalar el paquete [learnr](https://rstudio.github.io/learnr/index.html) utilizando el siguiente código:

``` r
install.packages("learnr")

```

y luego ejecutar de esta manera el Tutorial:

`learnr::run_tutorial("TextMining", package = "TextMiningTutorial")`


Como siempre, rspero que les sirva, se diviertan y aprendan. 