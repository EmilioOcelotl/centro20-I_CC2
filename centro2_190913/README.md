# Clase 5

## Processing

### ¿Qué hemos visto hasta el momento? 

### Sintaxis += y ++

Anteriormrente vimos algunas expresiones que simplifican el trabajo de escribir expresiones que son comunes en la programación. 

En este sentido, es necesario usar "atajos" de código que nos ayudan a tener un código más conciso. 

Por ejemplo, hay un operador que agrega el valor 1 a una variable (++) un operador que disminuye el valor uno a una variable (--=

```java
int x = 1;
println(x);
x++;
println(x);
```

```java
int y = 1; 
println(y);
y--; 
println(y); 
```

El valor se incrementa o decrece después de que la expresión se evalúa. El siguiente ejemplo demuestra esta situación. 

```java
int x = 1;
println(x++);
println(x);
```

Para actualizar el valor antes de que la expresión sea evaluada, hay que poner el operador al frente de la variable. 

```java
int x = 1;
println(++x);
println(x); 
```

El operador += combina suma e igualación de un valor. De igual forma existe el operador -= que resta al mismo tiempo que iguala un valor. 

```java
int x = 1;
println(x);
x += 5;
println(x); 
```

```java
int y = 1;
println(y);
y -= 5;
println(y);
```

Existen otros atajos como *= y /= que podemos deducir por el primer operador. 


### Contadores 

Los atajos antes vistos nos permiten abordar contadores. 

La clase pasada realizamos un contador relativamente sencillo que aumentaba en 1 el valor que le asignamos a la variable que controlaba el diámetro de los círculos. 

Entonces, cuando se ejecutaba `dia = dia + 1;` en draw() aumentabamos en 1 el tamaño del diámetro. 

Cada vuelta o cada cuadro del draw() aumenta día en uno. 

Este primer ejercicio es un contador bastante sencillo que nos ayuda a explorar las posibilidades del cambio en cada cuadro. 

Es posible limitar el comportamiento del contador, de forma tal que los valores de la variable que están transformando no se incrementen hasta el inifinito (o hasta que paremos el programa).

En el ejercicio pasado, eso lo realizamos con el operador %. Con esta operación podíamos "reiniciar" el valor de la variable que transformabamos con la suma en uno en cada vuelta. 

Resolvimos la limitación del comportamiento del contador con un if() e invirtiendo el valor de la operación multiplicando la variable que controlaba el diámetro por -1.

### Ejercicio de la clase de hoy

Reconstruiremos un ejercicio parecido al de la clase pasada, en esta ocasión utilizaremos otra figura y veremos si es posible agregar algún comportamiento en el color. 

### `loop()` y `noLoop()`

Como ya vimos, Processing *loopea* continuamente el código escrito en `draw()`. Sin embargo, el *loop* `draw()` puede detenerse cuando escribimos `noLoop()`. En ese caso, el loop `draw()` puede reanudarse con `loop()`; 

Ejemplo: 

```java 
void setup() {
  size(200, 200);
  noLoop();  // draw() will not loop
}

float x = 0;

void draw() {
  background(204);
  x = x + .1;
  if (x > width) {
    x = 0;
  }
  line(x, 0, x, height); 
}

void mousePressed() {
  loop();  // Holding down the mouse activates looping
}

void mouseReleased() {
  noLoop();  // Releasing the mouse stops looping draw()
}
```

### `for()`

Otra estructura de código llamada `for()` hace posible correr una de código más de una vez. Esto permite condensar una repetición en pocas líneas. 

El siguiente ejemplo dibuja un patrón 

```java
size(480, 120);
strokeWeight(8);
line(20, 40, 80, 80);
line(80, 40, 140, 80);
line(140, 40, 200, 80);
line(200, 40, 260, 80);
line(260, 40, 320, 80);
line(320, 40, 380, 80);
line(380, 40, 440, 80);
```

Que puede simplificarse de la siguiente manera: 

```java
size(480, 120);
strokeWeight(8);
for (int i = 20; i < 400; i += 60) {
line(i, 40, i + 60, 80);
}
```

Las llaves, es decir { y }, distinguen a `for()`. El código que se encuentra entre llaves se llama bloque. Este es el código que va a ser repetido en cada iteración del *loop* `for()`. 

Dentro de los paréntesis hay tres declaraciones separadas por punto y coma. De izquierda a derecha, estas declaraciones son: *init, test* y *update*

```java
for (init; test; update) {
statements
}
```
En *init* fijamos el valor inicial, muchas veces declarando una variable que usaremos dentro del loop for. 

El nombre de variable `i` es frecuentemente usado, pero no hay nada especial en él. 

*Test* evalúa el valor de esta variable (para el caso del primer código, revisa si `i` sigue siendo menor que 400). *Update* cambia el valor de la variable, agregando 60 antes de repetir el *loop*.

Un diagrama puede clarificar el flujo de un *for loop* 

Cabe destacar que la declaración *text* es siempre una expresión relacional que compara dos valores con un operador relacional. En el ejemplo de arriba, la expresión es "i < 400" y el operador es < (menor que). Los operadores relacionales más comunes son: 

| Símbolo | Operación        |
|:-------:|:----------------:|
| >       | Mayor que        | 
| <       | Menor que        |
| >=      | Mayor o igual que|
| <=      | Menor que        |
| ==      | Igual a          |
| !=      | No es igual a    |

El resultado de la evaluación siempre es cierto o falso. 

### Ejercicios para entregar dentro de dos semanas 
