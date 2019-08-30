# Clase 3. Lógica I

Terminar color, variables y operadores aritméticos. 

## Lógica proposicional

Es un sistema formal cuyos elementos más básicos representan proposiciones. Hay operaciones sobre preoposiciones que se llaman constantes lógicas. 

Es posible realizar encadenamientos de operaciones de forma tal que se general preposiciones de mayor complejidad. 

## Concepto de proposición

Una proposición expresa un contenido semántico a la que bajo cierto procedimiento acordado o prescrito es posible asignarle un valor de verdad (por el momento nos acotaremos a verdadero y falso). 

## Proposiciones compuestas: disyunción, conjunción, negación, condicional y bi-condicional

La siguiente tabla muestra las conectivas lógicas de la lógica proposicional. 

| Conectiva   | Expresión lenguaje formal| Operador en Processing |
|:-----------:|:------------------------:|:----------------------:|
| Conjunción   | y                        | &&                    |
| Disyunción   | o                        | &#124;&#124;          |
| Negación     | no                       | !                     |
| Condicional  | si... entonces           |                       |
| Bicondicional| Si y sólo si             |                       |

En Processing solamente es posible expresar por medio de operadores los primeros tres tipos de proposiciones. Más adelante en esta misma sesión revisaremos la forma en la que una proposición condicional puede implementarse en el contexto del despliegue de figuras en Processing. 

La siguiente tabla contiene las posibles combinaciones de conjunción, disyunción y negación. 

|Expresión|Evaluación|
|:-------:|:--------:|
|true && true|true|
|true && false|false|
|false && false|false|
|true &#124;&#124; true|true|
|true &#124;&#124; false|true|
|false &#124;&#124; false |false|
|!true|false|
|!false|true|

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

`boolean b = true;`

El ejemplo anterior puede utilizarse para el caso de las proposiciones antes mencionadas. 

Variables booleanas y los distintos estados del ratón como método de entrada. 

### Modo dinámico

Ya hemos mencionado que Processing tiene dos modos separados: activo y estático. 

El modo activo implica dos momentos o bloques de código: `setup()` y `draw()`. Básicamente, el código que escribimos dentro de `draw()` se actualiza 60 veces cada segundo. Esto permite que los objetos que dibujamos den la sensación de movimiento. 

Las funciones `setup()` y `draw()` hacen posible que el programa corra continuamente. Esto nos posibilita también animaciones y programas interactivos. 

El código dentro de `setup()` corre una vez cuando el programa inicia y el código dentro de `draw()` corre continuamente. 

Las próximos tópicos de la clase nos mostrarán como es posible aprovechar las posibilidades de la relación `setup()` y `draw()` en la ejecución continua de un programa. 

A continuación un ejemplo de la estructura del modo dinámico: 

```java
void setup() {
println("Inició setup");
}
void draw() {
println("Corre continuamente");
}
```

El ejemplo anterior no dibuja sino que imprime valores en la consola vía la función `println()`. Si ejecutamos el programa, luego lo detenemos y finalmente exploramos la consola de mensajes, podemos ver que el mensaje "Inició setup" se imprimió solamente una vez en cuanto inició el programa. Posteriormente, el mensaje "Corre continuamente" se imprime continuamente, con cada vuelta que da `javadraw()` y que se interrumpe en cuanto detenemos el programa. Hay otras formas de detener y reiniciar `draw()`. Más adelante en el curso las revisaremos. 

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

También podemos asignar los valores de la posición del mouse en X y Y a las posiciones de los objetos en Processing 

¿Cómo podríamos hacer esto?

Por último, hablaremos de mousePressed para clarificar lo que ya hemos mencionado sobre las variables booleanas. 

mousePressed es una especie de variable reservada que Processing lee por default. Width y Height también son variables que Processing entiende sin declararlas. 

Esta función se comporta como una variable booleana, si presionamos el botón izquierdo del mouse, entonces nos devolverá verdadero, si dejamos de presionarlo, nos devolverá falso. 

```java
void draw(){
println(mousePressed); 
}
```

### Condicionales simples

Las condicionales funcionan de manera parecida a las preguntas. Permiten a un programa realizar una acción si la respuesta a la pregunta es "cierto" o realizar otra acción si la respuesta es "falso". 

Las preguntas formuladas dentro de un programa son siempre declaraciones lógicas o relacionales. 

En el siguiente ejemplo tenemos el caso de dos condicionales para dos objetos. Si esta condición se cumple, entonces lo que se encuentra dentro de las llaves se ejecuta. Si no se cumple, el código no se ejecuta. 

Este es un caso específico de la estructura if. 

Para el caso de las condicionales del ejemplo ejecutado, hay expresiones relacionales que compara dos valores con un operador relacional. En el ejemplo de arriba, la expresión es "i < 400" y el operador es < (menor que). Los operadores relacionales más comunes son:

| Símbolo | Operación        |
|:-------:|:----------------:|
| >       | Mayor que        | 
| <       | Menor que        |
| >=      | Mayor o igual que|
| <=      | Menor que        |
| ==      | Igual a          |
| !=      | No es igual a    |


```java
x = 90

if (x < 100) {
rect(35, 35, 30, 30);
}

if (x > 100) {
ellipse(50, 50, 36, 36);
}


line(20, 20, 80, 80);

```

Entonces la estructura general de if es la siguiente: 

```java
if(test){
	statement
}
```

El siguiente ejemplo funciona en el contexto del modo dinámico de Processing. Noten que también utiliza else, la segunda parte de la condicional if. En este sentido, la condicional es un caso específico de la estructura if/else

```java
void setup() {
size(240, 120);
strokeWeight(30);
}
void draw() {
background(204);
stroke(102);
line(40, 0, 70, height);
if (mousePressed) { // aquí utilizamos mousePressed como una variable booleana
stroke(0);
} else {
stroke(255);
}
line(0, 70, width, 50);
}
```

Entonces la estructura general de if/else es: 

```java
if (test) {
	statements 1
} else {
	statements 2
}
```

### Formas básicas: triangle, arc, quad

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

Quad dibuja un polígono de cuatro lados. Si bien es similar a un rectángulo, los ángulos de un Quad no necesariamente están constreñidos a 90 grados. El primer par de parámetros definen el primer vértice del polígono y los pares subsiguientes definen la figura completa. 

Entonces, la sintaxis para dibujar esta figura es: 

`quad(x1, y1, x2, y2, x3, y3, x4, y4)` 

```java
quad(38, 31, 86, 20, 69, 63, 30, 76);
quad(20, 20, 20, 70, 60, 90, 60, 40);
quad(20, 20, 70, -20, 110, 0, 60, 40);
```
