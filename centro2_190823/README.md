
# Clase 2 | Fundamentos de computación y *Processing*

Clase pasada. 

## Fundamentos de computación y *Processing*

## ¿Qué es la computación?

## Processing

(Ya habíamos comentado algo de esto la clase pasada) 

Processing es un entorno de trabajo y un lenguaje de programación de código abierto basado en Java. 

Está enfocada a las artes electrónicas, al arte con nuevos medios y al diseño visual. 

Sus funciones principales tienen que ver con graficos pero tiene extensiones para audio y comunicación. 

Processing tiene ventajas: instalación sencilla, multiplaforma, librerías externas, se acopla a protocolos estándar. 

Processing es una introducción amigable al ámbito de la programación. 

### Instalación y ambiente

Processing se puede descargar de [https://processing.org/](https://processing.org/) 

En la sección Downloads se puede encontrar los archivos para Windows, Linux y Mac OS X. 

Al abrir el ejecutable se despliega el Entorno de Desarrollo Integrado (IDE) también conocido como Entorno de Desarrollo de Processing (PDE). 

![PDE](https://github.com/EmilioOcelotl/centro20-I_CC2/blob/master/img/pde.gif)

Una imagen de mejor calidad de los elementos del PDE se puede encontrar en la página 8 de *Processing. A Programming Handbook for Visual Designers and Artist.* 

### Aclaraciones iniciales

Las funciones son los los bloques basicos para construir programas en Processing. 

Algunas de ellas son *size()* *line()* *fill()* 

La modularidad es una de las características más importantes de las funciones en Processing. Son unidades de software independientes que pueden ser usadas para construir programas más complejos. 

### Modo estático

Processing tiene dos modos separados: activo y estático. 

El modo activo implica dos momentos o bloques de código: `setup()` y `draw()`. Básicamente, el código que escribimos dentro de `draw()` se actualiza 60 veces cada segundo. Esto permite que los objetos que dibujamos den la sensación de movimiento. 

El modo estático implica solamente una lista con instrucciones/llamadas a distintas funciones. Podemos dibujar pero no hay forma de que lo que dibujamos se refresque. 

### Comentarios

En Processing y en muchos otros entornos de trabajo, los comentarios son partes del programa que son ignorados cuando el programa corre. 

Cuando escribimos dobles barras (//) en el editor de Processing, agregamos un comentario que es ignorado hasta que hay un salto de línea. 

Los comentarios son útiles para dejar notas y explicar qué sucede en el código. También sirven para desactivar partes del código mientras boceteamos. 

Otra forma de comentar es: iniciar con /* y terminar con */. El siguiente ejemplo demuestra el funcionamiento del comentario. 

```java
// Los comentarios se distinguen del código activo por el coloreado del texto. Terminan cuando hay un salto de línea
size(400, 400);
/*
También es posible comentar texto o código con /* y */
Esto sirve para comentar bloques de código, en este caso, los saltos de línea no terminan el comentario
*/ 
```

### Coordenadas cartesianas: *pixel coordinates*

### Formas básicas: point, line, rectangle, ellipse

### Color: grayscale, RGB, HSB y transparencia

### Referencia y ayuda

### Qué es una variable: int, float

### Operadores aritméticos

## Ejercicios 
