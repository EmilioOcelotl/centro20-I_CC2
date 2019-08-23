
# Clase 2 | Fundamentos de computación y *Processing*

¿De qué hablamos la clase pasada? 

Zach Lieberman y la evolución de sus sketches. 

Nadar y la visión computarizada. 

## Fundamentos de computación y *Processing*

## ¿Qué es la computación?

Administrar métodos, técnicas y procesos con el fin de almacenar, procesar y transmitir información y datos en formato digital. 

## Processing

(Ya habíamos comentado algo de esto la clase pasada) 

En este curso vamos a revisar Processing (si nos da tiempo, veremos otras plataformas y acercamientos). 

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
// Los comentarios se distinguen del código activo por el coloreado del texto. 
// Terminan cuando hay un salto de línea
size(400, 400);
/*
De esta manera se comentan bloques de código 
En este caso, los saltos de línea no terminan el comentario
*/ 
```

### Coordenadas cartesianas: *pixel coordinates*

Para localizar un punto utilizamos coordenadas cartesianas. 

Processing parte de este prinicipio. El sistema de coordenadas de Processing es ligeramente distinto y utiliza algunos principios del procesamiento de imagen por medio de la computadora. 

Recordemos que la pantalla de una computadora es una cuadrícula de elementos que emiten luz llamados pixeles.

Escribimos las coordenadas de un pixel de la siguiente manera: (x, y)

A diferencia del sistema de coordenadas cartesianas (origen en el centro), Processing (y otros programas que se utilizan para dibujar pixeles en una pantalla) tienen el origen en la esquina superior izquierda. 

Por este motivo, el punto (0, 0) estará en la esquina superior derecha. 

Si invocamos una pantalla de 200x200 pixeles, la esquina superior izquierda es el origen, o sea (0, 0) y la esquina inferior derecha es (199, 199)

A continuación el código que despliega una pantalla para dibujar de 200x200 pixeles

```java
size(200, 200);
```

Como ya mencionamos, el coloreado indica cosas en Processing. Para el caso de size, el color azul indica que size es una función. 

Por el momento no nos detendremos a definir una función, ya que puede tener distintas definiciones. 

Mientras tanto, nos quedaremos con la explicación de una función en el contexto de Processing.

Las funciones son los los bloques basicos para construir programas en Processing. 

Algunas de ellas son *size()* *line()* *fill()* 

La modularidad es una de las características más importantes de las funciones en Processing. Son unidades de software independientes que pueden ser usadas para construir programas más complejos. 

Más adelante aprenderemos a escribir funciones para extender las capacidades de Processing más allá de sus características incorporadas. 

### Formas básicas: point, line, rectangle, ellipse

En Processing es posible escribir formas básicas como un punto, una línea, un rectángulo y un círculo. A partir de estos elementos es posible dibujar figuras más complejas. 

#### Point

Cada figura tiene parámetros específicos. 

El objeto más sencillo que podemos dibujar es un punto. 

Un punto tiene dos parámetros: posición en X y posición en Y. 

Dibujar un punto equivale a dibujar un pixel en el canvas de Processing. 

```java
point(30, 20);
point(85, 20);
point(85, 75);
point(30, 75);
```

#### Line 

En Processing, una línea se define a partir de la posición de dos puntos. Estos dos puntos se definen a su vez, por sus respectivas posiciones en X y Y. 

El siguiente ejemplo explica esto de manera general

`line(x1, y1, x2, y2)`

Una línea se dibuja definiendo la posición en X y en Y del primer punto y la posición en X y en Y del segundo punto. 

Ejemplo: 

```java
size(480, 120); // define el tamaño de la ventana
line(20, 50, 420, 110); // primer punto (20, 50) segundo punto (420, 110) 
```

En este modo de Processing, es posible dibujar múltiples objetos si escribimos como una lista. 

Pequeños ejercicios:

¿Cómo dibujaríamos dos líneas verticales y paralelas del mismo tamaño? 

#### Rect

En Processing es posible dibujar rectángulos de distintas formas. 

Por default, Processing nos pide 4 valores: los primeros dos son la posición del origen del rectángulo, los otros dos definen anchura y altura. El origen del rectángulo no está en el centro de la figura, sino en la esquina superior izquierda. 

El siguiente ejemplo explica de manera general los parámetros para dibujar un rectángulo

`rect(x, y, anchura, altura)`
 
 El siguiente ejemplo dibuja un rectángulo en Processing. 

```java
// Dibujar un rectángulo con punto inicial en (180, 60), ancho de 220 y alto de 40
size(480, 120);
rect(180, 60, 220, 40);
```

Pequeño ejercicio: Dibujar dos rectángulos del mismo tamaño, uno a la derecha y el otro a la izquierda de la pantalla. 

#### Ellipse

Ellipse puede dibujar círculos pero también elipses. Recibe cuatro parámetros; el primero y el segundo definen la posición en X y Y del centro de la figura. El tercero y cuarto definen anchura y altura. 

Un círculo se dibuja cuando los valores de anchura y altura son los mismos. 

`ellipse(x, y, anchura, altura)` 

El siguiente ejemplo dibuja un círculo. 

```java
size(480, 120);
ellipse(278, -100, 400, 400);
```

Ejercicio. De igual manera a los dos anteriores: ¿Cómo se dibujarían dos círculos del mismo tamaño, con la misma posición en Y y con posiciones diferentes en X? 

Otras formas son: `triangle, quad` y `arc.` 

#### Figuras diferentes y orden 

El orden de las instrucciones importa, en este ejemplo el rectángulo se dibuja encima del círculo debido a que aparece después en el código.

```java
size(480, 120);
ellipse(140, 0, 190, 190);
rect(160, 30, 260, 20);
```

En este otro, la elipse se encuentra encima debido a que aparece después 

```java
size(480, 120);
rect(160, 30, 260, 20);
ellipse(140, 0, 190, 190);
```

Ejercicio: Dibujar las cuatro figuras que vimos en diferentes posiciones, de forma tal que al menos una porción de cada una pueda ser visible en una ventana de 400x400. 

Nota: Es importante que guarden este ejercicio ya que con el trabajaremos los siguientes apartados. 

### Color: grayscale, RGB, HSB y transparencia

Hasta el momento hemos dibujado formas en blanco y negro y el fondo de la ventana se ha mantenido en gris claro. 

Para cambiar esto vamos a utilizar las funciones `background()` `fill` y `stroke`. 

Los valores de los parámetros tienen el rango de 0 a 255, donde 255 es blanco, 128 es un gris medio y 0 es negro. 

El siguiente ejemplo muestra tres diferentes valores en circulos que están sobre un fondo negro. 

```java
size(480, 120);
background(0); // negro
fill(204); // gris claro
ellipse(132, 82, 200, 200); // círculo gris claro
fill(153); // gris medio 
ellipse(228, -16, 200, 200); // círculo gris medio
fill(102); // gris oscuro
ellipse(268, 118, 200, 200); círculo gris oscuro
```

Es posible deshabilitar el contorno y el relleno con `noStroke()` y `noFill()`. 

```java
size(480, 120);
fill(153);
ellipse(132, 82, 200, 200);
noFill();
ellipse(228, -16, 200, 200);
noStroke();
ellipse(268, 118, 200, 200);
```

Si queremos usar valores más allá de la escala de grises, podemos usar tres parámetros para especificar los componentes de un color (rojo, verde y azu). 

```java
size(480, 120);
noStroke();
background(0, 26, 51);
fill(255, 0, 0);
ellipse(132, 82, 200, 200);
fill(0, 255, 0);
ellipse(228, -16, 200, 200);
fill(0, 0, 255);
ellipse(268, 118, 200, 200);
```

La definición de un color con la convención RGB proviene de la manera en que la computadora define colores en la pantalla. 

Los valores RGB se pueden definir en un rango que va de 0 a 255. 

Hay un cuarto valor que se puede utilizar para definir un valor de color. El valor alpha define transparencia. 

Este valor, como los que hemos visto hasta el momento, puede ir de 0 a 255 donde 0 define un color completalmente transparente y 255 un color completamente opaco. 

```java
size(480, 120);
noStroke();
background(204, 226, 225);
fill(255, 0, 0, 160);
ellipse(132, 82, 200, 200);
fill(0, 255, 0, 160);
ellipse(228, -16, 200, 200); 
27fill(0, 0, 255, 160);
ellipse(268, 118, 200, 200);
```

#### HSV o HSB  

Investigar este modelo de color

#### Ejercicios

Asignar un color distinto a cada una de las figuras que dibujamos en el ejercicio anterior. Al menos dos de ellas deben tener colores expresados en la convención RGB y dos de ellas deben tener transparencia. 

### Referencia y ayuda

En caso de que tengamos problemas con alguna función en específico, es posible consultar la referencia en línea. 

En esta documentación podemos encontrar una breve explicación de la función o del objeto en cuestión, qué parámetros recibe y un ejemplo de cómo puede implementarse. 

Link a las referencias

### Qué es una variable: int, float

Con variables asignamos valores específicos a espacios físicos de la computadora. En estos espacios podemos guardar, entre otras cosas, números. 

En processing, los números que podemos guardar en variables son de dos tipos: enteros y de punto flotante. 

Números enteros

Números de punto flotante.

En Processing es posible almacenar números en variables con las siguientes indicaciones: 

```java
int equis = 245;
float ye = 123; 

```

En muchos lenguajes de programación existe la convención de que todas las variables empiezan con minúscula. 

Esto debido a que en ciertas plataformas, los nombres de las clases empiezan con mayúscula. 

En Processing las variables empiezan con minúscula a pesar de que el nombre de las funciones como size() empiezan también con minúscula. 

Podemos asignar cualquier nombre a las variables, pero es importante que podamos darles nombres que identifiquemos.

### Operadores aritméticos

En términos de código, símbolos como +, - y * son operadores. Cuando aparecen entre dos valores, crean una expresión. 

Por ejemplo 5 + 9 y 1024 - 512 son ambas experesiones. 

Los operadores para realizar operaciones matemáticas básicas son: 

| Símbolo | Operación        |
|:-------:|:----------------:|
| +       | Suma             | 
| -       | Resta            |
| *       | Multiplicación   |
| /       | División         |
| =       | Igual a          |

Processing tiene una serie de reglas para definir que operadores tienen preferencia. Esto quiere decir que algunos cálculos se hacen primero, luego otros y luego otros. 

Estas reglas definen el orden de declaración del código cuando se ejecuta. 

Ejemplo:

```java
int x = 4 + 4 * 5; 
```

En este caso la operación 4 * 5 se evalúa primero debido a que la multiplicación tiene la prioridad más alta. Posteriormente, al producto de 4 * 5 se le agrega 4. 

Para forzar el orden de las operaciones se utilizan los paréntesis. Todo lo que está entre paréntesis se calcula primero. 

|
```java
int x = (4 + 4) * 5; 
```

Otros tipos de operaciones que son convenciones para ahorrar escritura: 

```java
x += 10; // es igual a x = x +10 
```

```java
x ++; // es igual a x = x + 1 
```
