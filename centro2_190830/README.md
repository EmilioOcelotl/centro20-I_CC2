# Clase 3. Lógica I

Terminar color, variables y operadores aritméticos. 

## Lógica proposicional

Es un sistema formal cuyos elementos más básicos representan proposiciones. Hay operaciones sobre preoposiciones que se llaman constantes lógicas. 

Es posible realizar encadenamientos de operaciones de forma tal que se general preposiciones de mayor complejidad. 

## Concepto de proposición

## Proposiciones compuestas: disyunción, conjunción, negación, condicional y bi-condicional

| Conectiva   | Expresión lenguaje formal| Operador en Processing |
|:-----------:|:------------------------:|:----------------------:|
| Conjunción   | y                        | &&                    |
| Disyunción   | o                        | &#124;&#124;          |
| Negación     | no                       | !                     |
| Condiciona   | si... entonces           |                       |
| Bicondicional| Si y sólo si             |                       |

En Processing solamente es posible expresar por medio de operadores los primeros tres tipos de proposiciones. 

La siguiente tabla contiene las posibles combinaciones de conjunción, disyunción y negación. 

|Expresión|Evaluación|
|:-------:|:--------:|
|true && true|true|
|true && false|false|
|false && false|false|
|true &#124;&#124; true|true|
|true &#124;&#124; false|true|
|false &#124;&#124; false |false|
|!true&#124;false|
|!false&#124;true|

Es posible realizar estas evaluaciones en Processing por medio de la función  `println()`. 

## Processing

Para determinar el flujo de información y de decisiones en Processing. 

### Variables booleanas

Processing puede almacenar y modificar diferentes tipos de datos. 

Estos pueden ser: números, letras, colores, imágenes, fuentes y valores booleanos. 

Los valores booleanos son aquellos que pueden tener "verdadero" o "falso" como valor. 

El dato más simple que existe en Processing es la variable booleana. Como ya mencionamos, estas variables pueden tener solamente uno de dos valores (cierto o falso). 

Las variables booleanas toman su nombre del matemático George Boole, inventor del algebra booleana, uno de los fundamentos de como funcionan las computadoras digitales. 

Una variable booleana por lo general se utiliza para tomar decisiones, por ejemplo, qué líneas de código son ejecutadas y cuales son ignoradas. 

### Modo dinámico

Ya hemos mencionado que Processing tiene dos modos separados: activo y estático. 

El modo activo implica dos momentos o bloques de código: `setup()` y `draw()`. Básicamente, el código que escribimos dentro de `draw()` se actualiza 60 veces cada segundo. Esto permite que los objetos que dibujamos den la sensación de movimiento. 

### Formas básicas: triangle, arc, quad, curve, modes

#### Triangle

Un triángulo es un plano creado al conectar tres puntos. Los primeros dos argumentos especifican el primer punto de ese plano, los dos siguientes el segundo, y los dos últimos el tercero. 

La sintaxis para dibujar un triángulo es la siguiente: 

`triangle(x1, y1, x2, y2, x3, y3)`

Un ejemplo de rectángulo: 

```java
triangle(55,9, 90, 80, 75, 90);
```

#### arc

Arc() dibuja un arco en la pantalla. Los arcos se dibujan a lo largo del borde exterior de una elipse definida por los parámetros a, b, c y d.

El origen de la elipse del arco se puede cambiar con la función ellipseMode (). Start y stop especifican los ángulos (en radianes) en los que se dibuja el arco. Los valores de inicio / parada deben estar en el sentido de las agujas del reloj.

Hay tres formas de dibujar un arco, se definen mediante el séptimo parámetro opcional. Las tres opciones son PIE, OPEN y CHORD. Por default, la opción OPEN está activdada.  

Sintaxis para dibujar un arco en Processing: 

``arc(a, b, c, d, start, stop)``
``arc(a, b, c, d, start, stop, mode)``

```java
arc(50, 50, 80, 80, 0, PI+QUARTER_PI, OPEN);
arc(50, 50, 80, 80, 0, PI+QUARTER_PI, CHORD);
arc(50, 50, 80, 80, 0, PI+QUARTER_PI, PIE);
arc(50, 55, 50, 50, 0, PI); 
arc(50, 55, 50, 50, radians(180), radians(180+90)); 
```
#### quad

quad(x1, y1, x2, y2, x3, y3, x4, y4)

#### curve

#### modes

### Condicionales simples

### Interacción con mouse: variables mouseX, mouseY

Es posible utilizar la entrada del mouse como una forma de controlar la posición y los atributos de las formas en la pantalla.

Historia del ratón. 

Tomemos en cuenta que la pantalla puede ser un puente entre los gestos de nuestro cuerpo y el conjunto de circuitos y electricidad que están dentro de la computadora. 

De entre los muchos dispositivos que existen para controlar elementos en la pantalla se encuentran el teclado y el ratón. 

El ratón como dispositivo se utiliza para controlar la posición de un cursor en pantalla y para seleccionar elementos. 

Cuando la computadora lee los valores de la posición del ratón, está leyendo dos valores: la coordenada en x y la coordenada en y. 

Si bien la lectura de estos dos elementos puede ser relativamente sencilla, también se puede extraer y analizar información de otro tipo, como la velocidad y la dirección. 

Este tipo de datos puede ayudarnos a reconocer gestos o parámetros.

Entender cómo funciona y cómo se puede utilizar en ratón en Processing puede ayudarnos a concebir relaciones de control entre cualquier entrada y el programa que realicemos. 
En Processing, las variables `mouseX` y `mouseY` (noten que X y Y se escriben con mayúsculas) almacenan los datos de la coordenada en X y la coordenada en Y del cursor. 

Esta posición es relativa al origen que se encuentra en la esquina superior izquierda de la pantalla. 

Podemos ver la posición actual de los valores producidos mientras movemos el mouse con el siguiente programa: 

```java
void draw() {
frameRate(12);
println(mouseX + " : " + mouseY);
}
```
