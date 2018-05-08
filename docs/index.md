<<<<<<< HEAD
# Álgebra
Synergy Vision  
`r Sys.Date()`  
<script src="https://cdn.datacamp.com/datacamp-light-latest.min.js"></script>

--- 
title: "Álgebra"
subtitle: "Ciencia de los Datos Financieros"
author: "Synergy Vision"
date: "2018-05-08"
=======
<script src="https://cdn.datacamp.com/datacamp-light-latest.min.js"></script>

--- 
title: "Álgebra Lineal"
subtitle: "Ciencia de los Datos Financieros"
author: "Synergy Vision"
date: "2018-05-07"
>>>>>>> 5fb01bf18b6aadb369125cd80053797b44d92989
knit: "bookdown::render_book"
documentclass: krantz
bibliography: [book.bib, packages.bib]
biblio-style: apalike
link-citations: yes
colorlinks: yes
lot: yes
lof: yes
fontsize: 12pt
monofontoptions: "Scale=0.8"
keep_md: yes
site: bookdown::bookdown_site
description: ""
url: 'http\://synergy.vision/Algebra/'
github-repo: synergyvision/Algebra/
cover-image: images/cover.png
---





# Prefacio {-}

<a href="https://synergy.vision/LibrosInteractivos/" target="_blank"><img src="images/cover.png" style="display: block; margin: auto;" /></a>


![Creative Commons License](images/by-nc-sa.png)  
La versión en línea de este libro se comparte bajo la licencia [Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License](http://creativecommons.org/licenses/by-nc-sa/4.0/).

## ¿Por qué  leer este libro? {-}

Este libro es el resultado de enfocarnos en proveer la mayor cantidad de material sobre Probabilidad y Estadística Matemática con un desarrollo teórico lo más explícito posible, con el valor agregado de incorporar ejemplos de las finanzas y la programación en `R`. Finalmente tenemos un libro interactivo que ofrece una experiencia de aprendizaje distinta e innovadora.

Es mucha la literatura, pero son pocas las opciones donde se pueda navegar el libro de forma amigable y además contar con ejemplos en `R` y ejercicios interactivos, además del contenido multimedia. Esperamos que ésta sea un contribución sobre nuevas prácticas para publicar el contenido y darle vida, crear una experiencia distinta, una experiencia interactiva y visual. El reto es darle vida al contenido asistidos con las herramientas de Internet.

Finalmente este es un intento de ofrecer otra visión sobre la enseñanza y la generación de material más accesible. Estamos en un mundo multidisciplinado, es por ello que ahora hay que generar contenido que conjugue en un mismo lugar las matemáticas, estadística, finanzas y la computación.

Lo dejamos público ya que las herramientas que usamos para ensamblarlo son abiertas y públicas.

## Estructura del libro {-}

## Información sobre los programas y convenciones {-}

Este libro es posible gracias a una gran cantidad de desarrolladores que contribuyen en la construcción de herramientas para generar documentos enriquecidos e interactivos. En particular al autor de los paquetes Yihui Xie xie2015.

## Prácticas interactivas con R {-}

Vamos a utilizar el paquete [Datacamp Tutorial](https://github.com/datacamp/tutorial) que utiliza la librería en JavaScript [Datacamp Light](https://github.com/datacamp/datacamp-light) para crear ejercicios y prácticas con `R`. De esta forma el libro es completamente interactivo y con prácticas incluidas. De esta forma estamos creando una experiencia única de aprendizaje en línea.

<div data-datacamp-exercise data-height="300" data-encoded="true">eyJsYW5ndWFnZSI6InIiLCJwcmVfZXhlcmNpc2VfY29kZSI6ImIgPC0gNSIsInNhbXBsZSI6IiMgQ3JlYSB1bmEgdmFyaWFibGUgYSwgaWd1YWwgYSA1XG5cblxuIyBNdWVzdHJhIGVsIHZhbG9yIGRlIGEiLCJzb2x1dGlvbiI6IiMgQ3JlYSB1bmEgdmFyaWFibGUgYSwgaWd1YWwgYSA1XG5hIDwtIDVcblxuIyBNdWVzdHJhIGVsIHZhbG9yIGRlIGFcbmEiLCJzY3QiOiJ0ZXN0X29iamVjdChcImFcIilcbnRlc3Rfb3V0cHV0X2NvbnRhaW5zKFwiYVwiLCBpbmNvcnJlY3RfbXNnID0gXCJBc2VnJnVhY3V0ZTtyYXRlIGRlIG1vc3RyYXIgZWwgdmFsb3IgZGUgYGFgLlwiKVxuc3VjY2Vzc19tc2coXCJFeGNlbGVudGUhXCIpIn0=</div>







## Agradecimientos {-}

A todo el equipo de Synergy Vision que no deja de soñar. Hay que hacer lo que pocos hacen, insistir, insistir hasta alcanzar. Lo más importante es concretar las ideas. La idea es sólo el inicio y solo vale cuando se concreta.


\BeginKnitrBlock{flushright}<p class="flushright">Synergy Vision, Caracas, Venezuela</p>\EndKnitrBlock{flushright}








<!--chapter:end:index.Rmd-->


# Acerca del Autor {-}

Este material es un esfuerzo de equipo en Synergy Vision, (<http://synergy.vision/nosotros/>).		 

El propósito de este material es ofrecer una experiencia de aprendizaje distinta y enfocada en el estudiante. El propósito es que realmente aprenda y practique con mucha intensidad. La idea es cambiar el modelo de clases magistrales y ofrecer una experiencia más centrada en el estudiante y menos centrado en el profesor. Para los temas más técnicos y avanzados es necesario trabajar de la mano con el estudiante y asistirlo en el proceso de aprendizaje con prácticas guiadas, material en línea e interactivo, videos, evaluación contínua de brechas y entendimiento, entre otros, para procurar el dominio de la materia.
  		  
Nuestro foco es la Ciencia de los Datos Financieros y para ello se desarrollará material sobre: **Probabilidad y Estadística Matemática en R**, **Programación Científica en R**, **Mercados**, **Inversiones y Trading**, **Datos y Modelos Financieros en R**, **Renta Fija**, **Inmunización de Carteras de Renta Fija**, **Teoría de Riesgo en R**, **Finanzas Cuantitativas**, **Ingeniería Financiera**, **Procesos Estocásticos en R**, **Series de Tiempo en R**, **Ciencia de los Datos**, **Ciencia de los Datos Financieros**, **Simulación en R**, **Desarrollo de Aplicaciones Interactivas en R**, **Minería de Datos**, **Aprendizaje Estadístico**, **Estadística Multivariante**, **Riesgo de Crédito**, **Riesgo de Liquidez**, **Riesgo de Mercado**, **Riesgo Operacional**, **Riesgo de Cambio**, **Análisis Técnico**, **Inversión Visual**, **Finanzas**, **Finanzas Corporativas**, **Valoración**, **Teoría de Portafolio**, entre otros.

Nuestra cuenta de Twitter es (https://twitter.com/bysynergyvision) y nuestros repositorios están en GitHub (https://github.com/synergyvision).
  		  
 **Somos Científicos de Datos Financieros**

<!--chapter:end:000-author.Rmd-->

\mainmatter

# Introducción 




<!--chapter:end:010-introduction.Rmd-->

# Estructuras algebraicas

<!--chapter:end:020-estructuras-algebraicas.Rmd-->

# Vectores

<!--chapter:end:030-vectores.Rmd-->

# Espacios vectoriales

<!--chapter:end:040-espacios-vectoriales.Rmd-->

# Matrices

<!--chapter:end:050-matrices.Rmd-->

# Autovalores y autovectores

<!--chapter:end:060-autovalores-autovectores.Rmd-->

# Cálculo en vectores y matrices

<!--chapter:end:070-calculo-vectores-matrices.Rmd-->

# Transformaciones lineales

<!--chapter:end:080-transformaciones-lineales.Rmd-->

# Producto escalar

<!--chapter:end:090-producto-escalar.Rmd-->

\cleardoublepage 

# (APPENDIX) Apéndice {-}

# Software Tools

For those who are not familiar with software packages required for using R Markdown, we give a brief introduction to the installation and maintenance of these packages.

## R and R packages

R can be downloaded and installed from any CRAN (the Comprehensive R Archive Network) mirrors, e.g., https://cran.rstudio.com. Please note that there will be a few new releases of R every year, and you may want to upgrade R occasionally.

To install the **bookdown** package, you can type this in R:


```r
install.packages("bookdown")
```

This installs all required R packages. You can also choose to install all optional packages as well, if you do not care too much about whether these packages will actually be used to compile your book (such as **htmlwidgets**):


```r
install.packages("bookdown", dependencies = TRUE)
```

If you want to test the development version of **bookdown** on GitHub, you need to install **devtools** first:


```r
if (!requireNamespace('devtools')) install.packages('devtools')
devtools::install_github('rstudio/bookdown')
```

R packages are also often constantly updated on CRAN or GitHub, so you may want to update them once in a while:


```r
update.packages(ask = FALSE)
```

Although it is not required, the RStudio IDE can make a lot of things much easier when you work on R-related projects. The RStudio IDE can be downloaded from https://www.rstudio.com.

## Pandoc

An R Markdown document (`*.Rmd`) is first compiled to Markdown (`*.md`) through the **knitr** package, and then Markdown is compiled to other output formats (such as LaTeX or HTML) through Pandoc.\index{Pandoc} This process is automated by the **rmarkdown** package. You do not need to install **knitr** or **rmarkdown** separately, because they are the required packages of **bookdown** and will be automatically installed when you install **bookdown**. However, Pandoc is not an R package, so it will not be automatically installed when you install **bookdown**. You can follow the installation instructions on the Pandoc homepage (http://pandoc.org) to install Pandoc, but if you use the RStudio IDE, you do not really need to install Pandoc separately, because RStudio includes a copy of Pandoc. The Pandoc version number can be obtained via:


```r
rmarkdown::pandoc_version()
## [1] '1.19.2.1'
```

If you find this version too low and there are Pandoc features only in a later version, you can install the later version of Pandoc, and **rmarkdown** will call the newer version instead of its built-in version.

## LaTeX

LaTeX\index{LaTeX} is required only if you want to convert your book to PDF. The typical choice of the LaTeX distribution depends on your operating system. Windows users may consider MiKTeX (http://miktex.org), Mac OS X users can install MacTeX (http://www.tug.org/mactex/), and Linux users can install TeXLive (http://www.tug.org/texlive). See https://www.latex-project.org/get/ for more information about LaTeX and its installation.

Most LaTeX distributions provide a minimal/basic package and a full package. You can install the basic package if you have limited disk space and know how to install LaTeX packages later. The full package is often significantly larger in size, since it contains all LaTeX packages, and you are unlikely to run into the problem of missing packages in LaTeX.

LaTeX error messages may be obscure to beginners, but you may find solutions by searching for the error message online (you have good chances of ending up on [StackExchange](http://tex.stackexchange.com)). In fact, the LaTeX code converted from R Markdown should be safe enough and you should not frequently run into LaTeX problems unless you introduced raw LaTeX content in your Rmd documents. The most common LaTeX problem should be missing LaTeX packages, and the error may look like this:

```latex
! LaTeX Error: File `titling.sty' not found.

Type X to quit or <RETURN> to proceed,
or enter new name. (Default extension: sty)

Enter file name: 
! Emergency stop.
<read *> 
         
l.107 ^^M

pandoc: Error producing PDF
Error: pandoc document conversion failed with error 43
Execution halted
```

This means you used a package that contains `titling.sty`, but it was not installed. LaTeX package names are often the same as the `*.sty` filenames, so in this case, you can try to install the `titling` package. Both MiKTeX and MacTeX provide a graphical user interface to manage packages. You can find the MiKTeX package manager from the start menu, and MacTeX's package manager from the application "TeX Live Utility". Type the name of the package, or the filename to search for the package and install it. TeXLive may be a little trickier: if you use the pre-built TeXLive packages of your Linux distribution, you need to search in the package repository and your keywords may match other non-LaTeX packages. Personally, I find it frustrating to use the pre-built collections of packages on Linux, and much easier to install TeXLive from source, in which case you can manage packages using the `tlmgr` command. For example, you can search for `titling.sty` from the TeXLive package repository:

```bash
tlmgr search --global --file titling.sty
# titling:
#	 texmf-dist/tex/latex/titling/titling.sty
```

Once you have figured out the package name, you can install it by:

```bash
tlmgr install titling  # may require sudo
```

LaTeX distributions and packages are also updated from time to time, and you may consider updating them especially when you run into LaTeX problems. You can find out the version of your LaTeX distribution by:



```r
system('pdflatex --version')
## pdfTeX 3.14159265-2.6-1.40.18 (TeX Live 2017)
## kpathsea version 6.2.3
## Copyright 2017 Han The Thanh (pdfTeX) et al.
## There is NO warranty.  Redistribution of this software is
## covered by the terms of both the pdfTeX copyright and
## the Lesser GNU General Public License.
## For more information about these matters, see the file
## named COPYING and the pdfTeX source.
## Primary author of pdfTeX: Han The Thanh (pdfTeX) et al.
## Compiled with libpng 1.6.29; using libpng 1.6.29
## Compiled with zlib 1.2.11; using zlib 1.2.11
## Compiled with xpdf version 3.04
```

<!--chapter:end:400-apendice.Rmd-->

# Referencias {-}




<!--chapter:end:500-references.Rmd-->

