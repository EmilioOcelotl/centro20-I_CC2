
# Clase 4 | Lógica II

## Recapitulación

¿Qué hemos visto hasta el momento? Formas, colores variables (hablaremos a profundidad de esto a continuación)  y operaciones. 

Aspectos del canvas que son importantes: size() y background(). 

Diferencia entre el modo estático y el modo dinámico en Processing. 

setup() y draw()

Podemos utilizar el modo dinámico como un loop. 

Interacción con el mouse. 

### Aclaración No. 1: Reglas para la declaración y elección de nombre de variables. 

Un repaso rápido de lo que son las variables: Una variable es un contenedor para almacenar datos. Las variables permiten utilizar datos muchas veces dentro de un programa. 

Una variable debe ser declarada antes de usarse. 

Atajo: Una variable puede ser declara y designada al mismo tiempo.

Lo importante para esta ocasión: las variables deben tener nombres que describan su contenido. Esto permite que el programa sea fácil de leer.

La designación del nombre de una variable es decisión del programador. 

Variables como t se deben usar al mínimo ya que por lo general son crípticas o en ciertos casos, se utilizan convencionalmente para ciertas cosas: tal es el caso de i que se utiliza para casos de iteración. 

Convenciones que ya hemos mencionado: deben iniciar con minúsculas y si hay más palabras en la asignación de la variable, la primer letra de cada palabra adicional debe estar en mayúsculas. 

Sin embargo, si cambiamos estas "reglas" Processing seguirá funcionando.

Hay reglas absolutas para la asignación de nombres de variables. 

Los nombres de las variables no pueden iniciar con números y no deben ser una palabra reservada. 

Algunos ejemplos de palabras reservadas son: int, if, true, null. 

Básicamente: los nombres de las variables no deben tener los mismos nombres de funciones que ya exsisten en Processing. 

También hay variables que por defecto, Processing ya declara y se pueden utilizar sin declararlas al inicio. 

### Aclaración No. 2: Módulo 

Hemos visto que Processing puede realizar operaciones con los caracteres +, -, *, / e =. 

Vamos a revisar rapidamente un símbolo nuevo que también puede realizar operaciones: módulo %

El operador % calcula el residuo cuando un número es dividido por otro. 

Entonces, %, el símbolo en notación de código para módulo, regresa el residuo entero que resulta de dividir el número que está a la derecha del símbolo entre el número de la derecha. 

|Expresión|Resultado|Explicación|
|:-------:|:-------:|:---------:|
|9 % 3    |0        |3 cabe tres veces en 9, sin residuo|
|9 % 2    |1        |2 cabe cuatro veces en 9, con un residuo de 1|
|35 % 4   |3        |4 entra ocho veces en 35, con un residuo de 3|

El operador módulo se utiliza con frecuencia para mantener números en un rango específico. 

Por ejemplo, una variable que se incrementa en uno cada vez (1, 2, 3, 4, 5, etc) puede transformarse con el operador módulo.

En este caso, si aplicamos % 4 el número que se incrementa continuamente puede producir un ciclo que oscila entre 0 y 3. 

|x  |0|1|2|3|4|5|6|7|8|9|10|
|---|-|-|-|-|-|-|-|-|-|-|-|
|x%4|0|1|2|3|0|1|2|3|0|1|2|
|---|-|-|-|-|-|-|-|-|-|-|-|

### Extra: Contadores sencillos

Para hacer interesantes los ejercicios que realizaremos en esta clase, vamos a ver un objeto muy sencillo que se puede realizar con tres elementos que ya hemos visto: variables, operaciones y draw().

```java
int contador = 0; 

void setup(){
size(600, 600); 
}

void draw(){

contador = contador + 1; // en cada vuelta del draw se agregará un elemento 
println(contador); // Recordemos que println imprime valores de lo que sucede en la consola

/*
Más adelante veremos contadores más complejos 

}
```

## Pequeño ejercicio 

Con lo que tenemos podríamos hacer un pequeño ejercicio que puede servir como plantilla para los ejercicios que deben entregar como forma de evaluación. 

- Primero explicar el modo loop con la elaboración de un contador sencillo que imprima valores en la consola. Hablar de las posibilidades de la consola.

- Guardar este valor en una variable que pueda funcionar en varias partes del código. 

- Dibujar algo que cambie dinámicamente en el draw(). 

- Utilizaremos el nuevo operador módulo (%). 

- Utilizaremos contadores para cambiar valores que esta vez no imprimiremos en la consola, sino que modificarán parámetros de los objetos dibujados. 

Alcanzamos a revisar la estructura if(). Este tipo de estructura o condicional es el el primer paso para empezar a revisar estructuras de control en Processing. 

## Tablas de verdad y evaluación de expresiones

La clase pasada revisamos que en processing resulta útil utilizar variables booleanas y hacer comparaciones del tipo true/false. 

Revisamos las proposiciones lógicas y señalamos que es posible realizar ejemplos relacionados a esto en Processing. 

También repasamos las posibles combinaciones de proposiciones compuestas y como esto se puede expresar en la lógica de Processing. 

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

## Tautologías, contradicciones y contingencias

Entender la lógica de Processing nos puede ayudar a resolver problemas relacionados con contradicciones en el código. 

Mostrar un ejemplo de contradicción con el ejemplo que hasta el momento hemos utilizado. 

## Equivalencias lógicas

## Processing

### Lectura de errores y Debugging

Recordar que Processing es un lenguaje, un generador de gráficos y también el entorno de desarrollo que parece un editor de texto.

Sintaxis, coloreado y señalamientos desde el mismo editor de texto.

Recordemos que la computadora lee una sintaxis que permiten que las instrucciones y funciones se realicen como las indicamos. 

Si hay un error en la sintaxis y tratamos de ejecutar el programa, Processing no desplegará una pantalla y nos arrojará mensajes en la consola. 

Hasta el momento hemos utilizado la consola para imprimir mensajes, como por ejemplo la evaluación de expresiones o el cambio dinámico de variables (bool o int/float). 

La consola también es el "interlocutor" que nos indicará que el programa fallo pero también dónde puede estar la causa del error. 

En este sentido, la lectura de errores se realizará por medio de la consola. 

Para encontrar errores es posible hacer una lectura rápida del código. Afortunadamente, Processing subraya con rojo la posible posición del error. 

A la práctica que se vale de estrategias (asistidas por el editor/entorno de trabajo o realizadas a simple vista) para encontrar errores en el software y resolverlos se le llama depuración de programas o debugging. 

En este sentido, un bug es el error que buscamos y que pretendemos depurar. 

Dato curioso: Una anécdota atribuye el término a Grace Hopper en 1940. Cuando trabajaba en la computadora Mark II en la Universidad de Harvard, descubrió un bicho atorado que obstaculizaba la operación de la computadora. Cuando ella intentó hacer funcional la computadora, mencionó que estaba "debuggeando" el sistema. 

Pero bueno, en otros contextos y en otros ámbitos prácticos se ha utilizado la palabra bug para designar a los errores. 

Una estrategia de debuggeo que hemos visto hasta el momento: imprimir en la consola con println(). 

### Condicionales completas

Breve repaso de lo que estudiamos sobre condicionales. Para el ejercicio que hasta el momento hemos realizado, la condicional es simple. 

Entonces, vamos a agregarle complejidad con la siguiente estructura: 

```java
if (test) {
	statements 1
} else if (test2) {
	statements 2
}
```

### (Más) Ejercicios 

¿Qué pasa si queremos dibujar más círculos? 

Podemos dibujarlos a mano con lo que sabemos, pero qué pasa si tenemos que dibujar 100 círculos.

Esto conducirá a un nuevo tipo de estructura que veremos la próxima clase: for(); 
