---
layout:     	slide
title:     		Introducción a la Programación
author:     	Dra. María de Los Ángeles Cosío León
tags:         Programación Clases fiad UABC
subtitle:    	"Generalidades de Clase y Conceptos Iniciales"

theme:		sky # default/beige/blood/moon/night/serif/simple/sky/solarized
trans:		cube # default/cube/page/concave/zoom/linear/fade/none

horizontal:	</section></section><section markdown="1" data-background=""><section markdown="1">
vertical:		</section><section markdown="1">
---
<section markdown="1" data-background=""><section markdown="1">
## {{ page.title }}

<hr>

#### {{ page.author }}

#### {{ page.date | | date: "%I %M %p ,%a, %b %d %Y"}}

{{ page.horizontal }}
<!-- Start Writing Below in Markdown -->

## Generalidades

* Exámenes Parciales: 60%
* Tareas: 10%
* Departamental: 30%

---

Sólo podrán realizar el examen parcial correspondiente las personas que tengan el *ticket* de acceso. Éste se definirá durante el avance de la materia.


{{ page.horizontal }}

### Para Controlar Ésta Presentación
---

* Presiona la tecla *Esc* para ver todas las "diapositivas"
* Presiona la tecla *B* para pausar la presentación
* Algunas diapositivas tienen más información en diapositivas "verticales", situadas inmediatamente arriba o abajo de la misma, aparece indicado en los controladores y cuando ves todas las diapositivas.

{{ page.horizontal }}
# Herramientas
---

Entorno de desarrollo: Lenguaje C estructurado.

* El IDE de referencia: Dev C++
* PSEINT

{{ page.horizontal }}

# Entrando en Materia

{{ page.horizontal }}

## Paradigmas de la Programación

* Paradimga Functional
* Paradigma Lógico
* Paradigma imperativo o procedural
* Paradigma orientado a objetos

---

Un paradigma define un conjunto de reglas, patrones y estilos de programación que son usados por un grupo de lenguajes de  programación.

{{ page.vertical }}

## Paradigma Functional

* La computación se realiza mediante la evaluación de expresiones
* Definición de funciones
* Funciones como datos primitivos
* Valores sin efectos laterales, no existe la asignación
* Programación declarativa
* Lenguajes: LISP, Scheme, Haskell, Scala


{{ page.vertical }}

## Paradigma Lógico

* Definición de reglas
* Unificación como elemento de computación
* Programación declarativa
* Lenguajes: Prolog, Mercury, Oz.

{{ page.vertical }}

## Paradigma Imperativo

* Definición de procedimientos
* Definición de tipos de datos
* Chequeo de tipos en tiempo de compilación
* Cambio de estado de variables
* Pasos de ejecución de un proceso

{{ page.vertical }}

## Paradigma Orientado a Objetvos

* Definición de clases y herencia
* Objetos como abstracción de datos y procedimientos
* Polimorfismo y chequeo de tipos en tiempo de ejecución
* Lenguajes: Java

{{ page.horizontal }}

## Metodología para la Solución de Problemas

1. Definición del problema
1. Análisis del problema
1. Algoritmo de solución del problema
2. Diagrama de flujo como herramienta para la resolución del problema
5. Codificación
8. Depuración

{{ page.vertical }}

Use MathJax for Math.

$$ A = \pi r^2 $$

{{ page.horizontal }}

# Lists

1. Item 1

2. Item 2

3. Item

{{ page.horizontal }}

# Links

[In-Line](https://www.google.com)

[I'm a reference-style link 1][1]

[I'm a reference-style link 1][2]

[1]:https://www.mozilla.org
[2]:http://www.reddit.com

{{ page.horizontal }}

# Images

Alt-Click to zoom.

![Description](http://projectpages.github.io/project-pages/img/Logo_Fairy_Tail_right.png)

{{ page.horizontal }}

# Code

Inline `code`.

{{ page.vertical }}

# Code Block

	import numpy as np
	def _set_colors():
    HighRGB = np.array([26, 152, 80]) / 255.

{{ page.horizontal }}

# Quotes

> War does not decide who is right, only who is **left**.

{{ page.horizontal }}

# HTML

Now, you CAN write in HTML using this template. If you want to create HTML presentations using this framework head over to [reveal.js](http://lab.hakim.se/reveal-js/#/) for reference.  For a power-point like interactive tool for creating presentations with this theme, check [slides.com](http://slides.com/).

{{ page.vertical }}

# Some HTML Functionality

## Color and Alignment

<p align="center">This text is centered.</p>

<p style="color:red">This is a red text with <span style="color:blue">blue</span> and <span style="color:green">green</span> inline text.</p>

{{ page.horizontal }}

## STL

<div align="center"><script src="https://embed.github.com/view/3d/projectpages/project-pages/gh-pages/stl/test.stl"></script></div>

{{ page.horizontal }}

## Data Projector

<embed src="/project-pages/2016/05/02/New-Projector/" height="500px" width="100%">

<!-- End Here -->
{{ page.horizontal }}

# [Print]({{ site.url }}{{ site.baseurl }}{{ page.url }}/?print-pdf#)

# [Back]({{ site.url }}{{ site.baseurl }})

</section></section>
