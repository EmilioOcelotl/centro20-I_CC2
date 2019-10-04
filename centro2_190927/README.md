# Clase 7

Repaso de todo lo visto.

El resultado fue: 

```java
/*
Modo Estático
Distintos bloques de código
*/ 

// comentario

// Inicia programa
// Declara variables

int posX;
float diametro;
float verde;
int cambioGradual; 

// Realiza instrucciones
// Preliminares

void setup(){ // se mantenga estática

size(600, 600);
frameRate(60); 
background(0); 
posX = 150; 
diametro = 30; 
verde = 150;

}

void draw(){ // loop
 // cambioGradual = 0;
 cambioGradual = cambioGradual + 1; // 1, 2, 3, 4, 5, 6, 7.. inf
 
 // 255, 254 .. 0;
 // contendedor parecido a módulo 
 
 if(cambioGradual == 256){
   cambioGradual = cambioGradual * -1;
 }
 
  //println(abs(cambioGradual));
  //verde = random(255); 
 //println(verde); 
 noStroke(); 
 //fill(255, verde, 0); // RGB 
 fill(255, abs(cambioGradual), 0); // 0 - 255
 ellipse(posX, 150, diametro, diametro); // dibuja esta linea
 ellipse(posX*2, 150, diametro, diametro); // dibuja esta linea

}

 // determina tamaño de la ventana
// dibuja si es importante el orden
//background(0); 
// ellipse(300, 300, 30, 30); // ignora esta linea
//verde = random(255); // min 0 max el valor de la función
//println(verde); 
// verde = random(150, 255);
//fill(255, verde, 0); // RGB 
//ellipse(posX, 150, diametro, diametro); // dibuja esta linea
//ellipse(posX*2, 150, diametro, diametro); // dibuja esta linea
// termina programa 
```
