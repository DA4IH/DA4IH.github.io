---
layout:     post
title:      Cellular Automatas and Medical Images
author:     Gener Avilés R
tags: 		  Autómatas imágenes medicina
subtitle:  	
category:  med
header-img: "img/med.png"
visualworkflow: true
---

Cellular Automata (CA) are models that are <a href="https://en.wikipedia.org/wiki/Discrete_mathematics"> discrete </a> in time and space, also known as tessellation automata, homogenous structures, cellular structures, iterative arrays, etc.
Mathematically, they can be defined as a 3-tuple where N is a set containing the neighborhood values, S is a set containing the possible states and <i>delta</i> being the transition function.

Mathematically, they can be defined as a 3-tuple where N is a set containing the neighborhood values, S is a set containing the possible states and <i>delta</i> being the transition function.
Cellular Automata (CA) are models that are <a href="https://en.wikipedia.org/wiki/Discrete_mathematics"> discrete </a> in time and space, also known as tessellation automata, homogenous structures, cellular structures, iterative arrays, etc.

<p style="text-align:center;"><i>CA={S,N,delta}</i></p>

In the medical world, CA are used to mimic tumor growth, data encryption, image processing, among others.

It is this last application that caught the attention of a friend of mine and I at a discrete mathematics class here at school. We were given a paper by <a href= "http://yadda.icm.edu.pl/yadda/element/bwmeta1.element.baztech-6e271df5-f264-47c9-9017-d6808ff2f1b4"> Płaczek </a> where CA are used to find the edges images or components of images. This has tremendous implications in the medical datasphere, it could be applied in the automation of the analysis of <a href= "http://www.medical-labs.net/normal-blood-smear-649/">blood smear samples </a>, <a href= "http://boneandspine.com/types-fracturesa-simple-classification-fractures-long-bones/">francture identification </a>, <a href="http://www.crios.be/genotoxicitytests/micronucleus_test.htm">genetic damage evaluated through micronucleus </a>, etc, etc, etc.

We set out to propose a CA with the least amount of rules possible that still could do a decent job at identifying fractures of long bones. After going over some theory and long hours of discussion, two rules emerged as the winners for this automaton, we decided that our CA was going to work on binary (black & white) images and identify borders in the objects of the image.
In order for the rules to be understood we have to declare some concepts before:
<ul>A greyscale image can be represented by a matrix of data<i> F={W x M} </i>where<i>F<sub>W,M</sub> belong to the set of numbers <i>{0,1,2,...,255}.</i></i> </ul>
The following image summarises the rules:

![Reglas del AC](https://raw.githubusercontent.com/DA4IH/DA4IH.github.io/master/img/carules.png)

<i>N </i>being a matrix of <i>3x3.</i>

With this approximation we were able to obtain preliminary results that reflected the power of working with a CA showing significant results with simple rules.

I will just show you one image of what this CA can produce, on the left you will see an image of an X-Ray of a femur with an oblique fracture, the next image is the binary version of the first. The one on the right hand side is an image produced entirely by the cellular automaton designed by us.

![Resultados](https://raw.githubusercontent.com/DA4IH/DA4IH.github.io/master/img/fractura.png)

As you can see, it was able to find the borders of the structured represented in the original image. Even though it is impossible to miss this fracture, the fact that a mathematical model with <i>just</i> two rules can generate this is impressive and talks to the potential for it's use in more advanced applications.

So far so good, I will keep experimenting and sharing with you what pops up.

Till the next one!

*If you want to try with your own images, you can try with the MatLab code we wrote for this:*

{% highlight matlab %}
clc
close all
clear
a=imread('NAME OF IMAGE');
a=rgb2gray(a);
tamano=size(a);
x=zeros(tamano(1),tamano(2));
for k=1:tamano(1)
    for l=1:tamano(2)
        if a(k,l)<128
            x(k,l)=0;
        else
            x(k,l)=255;
        end
    end
end
subplot(1,3,1)
imshow(a);
subplot(1,3,2)
imshow(x);
y=zeros(tamano(1),tamano(2));
y=y+255;
for k=1:tamano(1)
    for l=1:tamano(2)
        if k>1 & k< tamano(1)-1 & l>1 & l<tamano(2)-1
            if x(k-1,l-1) == 0 & x(k,l-1) == 0 & x(k+1,l-1) == 0 & x(k-1,l) == 0 & x(k,l) == 0 & x(k+1,l) == 0 & x(k-1,l+1) == 0 & x(k,l+1) == 0 & x(k+1,l+1) == 0
                c(k,l)=255;
            else
            if x(k-1,l-1) == 255 & x(k,l-1) == 255 & x(k+1,l-1) == 255 & x(k-1,l) == 255 & x(k,l) == 255 & x(k+1,l) == 255 & x(k-1,l+1) == 255 & x(k,l+1) == 255 & x(k+1,l+1) == 255
               y(k,l)=255;
            else
                y(k,l)=0;
            end
            end
        end
    end
end
subplot(1,3,3)
imshow(y);
}{% endhighlight %}
