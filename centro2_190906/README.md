
# Clase 4 | Lógica II

## Recapitulación

¿Qué hemos visto hasta el momento? Formas, colores, variables y operaciones. 

Aspectos del canvas que son importantes: size() y background(). 

Reglas para la declaración y elección de nombre de variables. 

Diferencia entre el modo estático y el modo dinámico en Processing. 

Podemos utilizar el modo dinámico como un loop. 

## Módulo 

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

## Pequeño ejercicio 

Con lo que tenemos podríamos hacer un pequeño ejercicio que puede servir como plantilla para los ejercicios que deben entregar como forma de evaluación. 

- Primero explicar el modo loop con la elaboración de un contador sencillo que imprima valores en la consola. Hablar de las posibilidades de la consola.

- Guardar este valor en una variable que pueda funcionar en varias partes del código. 

- Dibujar algo que cambie dinámicamente en el draw(). 

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

## Evaluación de expresiones

## Tautologías, contradicciones y contingencias

Entender la lógica de Processing nos puede ayudar a resolver problemas relacionados con 

## Equivalencias lógicas

## Processing

### Lectura de errores y Debugging

Recordar que Processing es un lenguaje, un generador de gráficos y también el entorno de desarrollo que parece un editor de texto

Sintaxis, coloreado y señalamientos desde el mismo editor de texto.

### Condicionales completas

### Ejercicios 
