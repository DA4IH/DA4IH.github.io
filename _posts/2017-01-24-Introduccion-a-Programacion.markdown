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
* [PSeInt](http://pseint.sourceforge.net)

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

## Definición del Problema
---

Está dada en sí por el enunciado del problema, el cual debe ser claro y completo. Es importante que conozcamos exactamente "qué se desea obtener al final del proceso".

> * ¿Qué entradas se requieren?
(Tipo y cantidad)
* ¿Cuál es la salida deseada?
(Tipo y cantidad)
* ¿Qué método produce la salida deseada?

{{ page.vertical }}

## Análisis del Problema

El propósito del análisis del problema es ayudar al programador a obtener una cierta comprensión de la naturaleza del problema.

---

* El problema debe estar bien definido si se quiere llegar a una solución satisfactoria.
* Para definir con precisión el problema se requiere que las especificaciones de entrada y salida sean descritas en detalle.
* Éstos son los requisitos mas importantes para llegar a una solución eficaz.

{{ page.vertical }}

## Análisis del Problema -- Ejercicio

> Se desea obtener una tabla de depreciaciones acumuladas y dos valores reales de cada año de un automóvil comprado en 1,800,000 pesos en el año de 2006, durante los seis años siguientes suponiendo un valor de recuperación de 120,000. Realizar el análisis del problema, conociendo la fórmula de la depreciación anual constante D para cada año de vida útil.

{{ page.vertical }}

## Análisis del Problema -- Solución
---

$$ D = {\dfrac{costo - valorDeRecuperación}{vidaÚtil}} $$

{{ page.horizontal }}

## Algoritmo

* El conjunto de instrucciones ordenadas, que especifican una secuencia finita de operaciones a realizar para resolver  una clase de problema.
* **Los algoritmos son más importantes que los lenguajes de programación o las computadoras**. Un lenguaje de programación es tan sólo un medio para expresar el algoritmo, y una computadora es sólo un procesador para ejecutarlo.

{{ page.horizontal }}

## Representaciones de un Algoritmo

Todo algoritmo puede ser representado por:

- Lenguaje natural
- Pseudocódigo
- Diagramas de flujo
- Lenguajes de programación

{{ page.vertical }}

## Lenguaje natural -- Ejemplo
---


* **Problema: Sumar 2 números.**
  - Inicio Suma
  - Ingresar primer número
  - Guardar número en variable a
  - Ingresar segundo número
  - Guardar número en variable b
  - Sumar a y b
  - Guardar resultado en R
  - Mostrar R
  - Fin


{{ page.vertical }}

## Pseudocódigo
---

* Es una forma de representar un algoritmo, que se acerca a los lenguajes de programación y con elementos del lenguaje natural.

* El pseudocódigo se compone de:
  - Cabecera
  - Declaraciones
  - Cuerpo
* La cabecera es la parte del algoritmo que posee el nombre de éste.
* Las declaraciones son las variables y constantes que utilizará el algoritmo para resolver el problema.
* El cuerpo son el conjunto de instrucciones o acciones que están entre el Inicio y el Fin.

{{ page.vertical }}

## Pseudocódigo

### Tipos de datos

---

- ***`num`***: cualquier número
- ***`BOOL`***: solo se le pueden asignar dos valores, y corresponden a falso/verdadero (*boolean*)
- ***`char`***: representa un carácter
- ***`arreglo`***: lista estática de elementos (*array*). Se debe de indicar el tipo y la cantidad de elementos que almacena.
- ***`string`***: conjunto de caracteres
- ***`nada`***: Ausencia de parámetros (para la entrada y/o para la salida).

{{ page.vertical }}

## Pseudocódigo

### Ejemplo

---

* La estructura del pseudocódigo es como sigue:

~~~
  Proceso SinTitulo
    accion 1;
    accion 2;
    .
    .
    .
    accion n;
  FinProceso
~~~

---

  - La sección "`Proceso SinTitulo`" es la cabecera del algoritmo
  - La sección "`accion 1, accion 2, ...`" es el cuerpo del algoritmo

{{ page.vertical }}

En este caso como utilizaremos el [PSeInt](http://pseint.sourceforge.net) la sección de declaraciones del algoritmo no se toma en cuenta, ya que el software se encarga de asignarle el tipo de dato a cada variable dependiendo del uso que se le dé.

{{ page.vertical }}

## Representación por Pseudocódigo de una Suma

~~~
Proceso Suma
    Escribir 'INGRESE PRIMER NÚMERO'
    Leer a;
    Escribir 'INGRESE SEGUNDO NÚMERO'
    Leer b;
    c<- a+b;
    Escribir 'LA SUMA ES:',C;
FinProceso
~~~

{{ page.horizontal }}

## Diagrama de Flujo

La representación mediante diagrama de flujo es una descripción gráfica de un algoritmo utilizando símbolos.

---

![Diagrama de Flujo](http://projectpages.github.io/project-pages/img/Logo_Fairy_Tail_right.png)

{{ page.horizontal }}
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
	def  _set_colors():
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
