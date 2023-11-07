# "Investigacion"

## pep8

### ¿que es?

La PEP8 es una guía que indica las convenciones estilísticas a seguir para escribir código Python. Se trata de un conjunto de recomendaciones cuyo objetivo es ayudar a escribir código más legible y abarca desde cómo nombrar variables, al número máximo de caracteres que una línea debe tener, este se encuentra en python.org. 

De acuerdo con Guido van Rossum, el código es leído más veces que escrito, por lo que resulta importante escribir código que no sólo funcione correctamente, sino que además pueda ser leído con facilidad. Esto es precisamente lo que veremos en este artículo.

Se trata de un conjunto de recomendaciones cuyo objetivo es ayudar a escribir código más legible y abarca desde cómo nombrar variables, al número máximo de caracteres que una línea debe tener.

## modulos y paquetes

### ¿que es?

Un **módulo** es un archivo de Python cuyos objetos (funciones, clases, excepciones, etc.) pueden ser accedidos desde otro archivo. Se trata simplemente de una forma de organizar grandes códigos.

***Ejemplo***

- Por ejemplo, un archivo aritmetica.py que contenga las siguientes definiciones:

def sumar(a, b):
    return a + b

def restar(a, b):
    return a - b

def mult(a, b):
    return a * b

def div(a, b):
    return a / b

- Podemos acceder a ellas desde otro archivo de Python ubicado en la misma ruta importando el módulo.

import aritmetica

print(aritmetica.sumar(7, 5))

- O bien, para importar todos los objetos dentro de un módulo:

from aritmetica import *

Un **paquete** es una carpeta que contiene varios módulos. 

***Ejemplo***

Siguiendo el ejemplo anterior, podemos diseñar un paquete matematica creando una carpeta con la siguiente estructura.

matematica/

    |-- __init__.py
    |-- aritmetica.py
    |-- geometria.py

- Debe contener siempre un archivo __init__.py (por el momento vacío) para que Python entienda que se trata de un paquete y no de una simple carpeta. Así, podemos acceder a alguno de los módulos del paquete de la siguiente manera.

import matematica.aritmetica

print(matematica.aritmetica.sumar(7, 5))

- O bien de la siguiente.

from matematica import aritmetica

print(aritmetica.sumar(7, 5))

## Entornos virtuales de python

### ¿que es?

Un entorno virtual es un entorno Python en el que el intérprete Python, las bibliotecas y los scripts instalados en él están aislados de los instalados en otros entornos virtuales, y (por defecto) cualquier biblioteca instalada en un «sistema» Python, es decir, uno que esté instalado como parte de tu sistema operativo.