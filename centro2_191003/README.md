
# Clase 8 

Hasta el momento hemos visto setup() y draw(). 

Hemos visto que es posible dar animación a los objetos en Processing con un contador. 

Podemos agregar un limitador con if() para que ese contador tenga un comportamiento y no solamente aumente hasta el infinito.

Vimos que es posible realizar esto también con la operación módulo. 

Hay una función específica que se llama random() que sirve para arrojarnos valores aleatorios. 

Hemos utilizado esta función para generar valores aleatorios, por ejemplo. 

En esta clase vamos a revisar detenidamente algunas funciones específicas de aleatoriedad. 

Al final veremos cómo es posible utilizar algún ejemplo de aleatoriedad en el contexto de la repetición con for().

Para realizar esto, haremos ejercicios sencillos con for(). 

## Aclaración previa

Estamos a la mitad del curso. 

Dentro de dos semanas ustedes realizarán la segunda entrega sujeta a evaluación. 

Como estamos revisando temas relativamente nuevos, vamos a realizar estos ejercicios en clase. 

En esta ocasión vamos a revisar algunos elmentos fundamentales que deberán estar incorporados en sus ejercicios, pero destinaremos las siguientes dos sesiones en trabajar proyectos y códigos específicos.

Las próximas dos sesiones ustedes generarán dos códigos que serán parte del mismo proyecto. La idea es que puedan enviarme estos dos códigos para tenerlos en cuenta para la entrega final que realizarán. 

Idealmente sus entregas deberán contar con un contador, con un if que lo controle y con manipulaciones de posición, tamaño o color. 

Adicionalmente sus entregas deberán tener aspectos de aleatoriedad y ruido, que veremos en esta ocasión. 

De manera optativa sus ejercicios deberán tener la estructura for(). En esta ocasión no es obligatorio pero para la tercera y para la última evaluación, será importante que puedan utilizar y explicar el funcionamiento de un for() en el contexto de Processing. 

## Aleatoriedad y ruido. 

Es posible incluir aleatoriedad y ruido en la composición visual. Existen varios ejemplos que utilizan el azar como un elemento que delimita algunos aspectos de la composición. 

Es posible tener una demostración completamente aleatoria del comportamiento del ciertas funciones en processing, por ejemplo:

```java
float posX;
float posY; 
float velX;
float velY; 

void setup(){
  size(600, 400);
  background(0);
  posX = random(600);
  posY = random(300);
  velX = random(20);
  velY = random(20);
}

void draw(){
  
  posX = posX + velX;
  posY = posY + velY;
  
  if((posX > width) || (posX < 0)){
    velX = velX * -1;
  }
  
  println(posX);
  
    if(posY > height || posY < 0){
    velY = velY * -1;
  }
  
  
  noStroke();
  fill(random(255), random(255), random(255), 200); 
  ellipse(posX, posY, 40, 40);
  
}
```

Recoredemos que la función `random()` se usa para crear valores impredecibles en un rango específicado por parámetros.

```java
random(valor más alto);
random(valor más bajo, valor más alto); 
```

Cuando solamente escribimos un parámetro en la función `random()`, ésta regresa un número de punto flotante que puede ir de cero al (pero no lo incluye)  valor del parámetro.

Si utilizamos dos parámetros, la función regresa un valor que se encuentra entre esos dos parámetros. 

## Ejercicio

Hacer una matriz de cuadros para demostrar la repetición y el cambio con for pero también el cambio de valores aleatorios. 
