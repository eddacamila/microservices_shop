# microservices Shop- MICROTIENDA CON MICROSERVICIOS


# Fat Ball o Monstruo come círculos. :basketball:
Ejemplo de aplicación de patrones de diseño a un juego básico.

## Demo Temporal 👽
[Ver Demo ](https://imasdyd.com/Juego_PatronesDiseno/)

## Contexto del Juego
Con esta sencilla aplicación de Javascript apoyado de canvas queremos simular una aproximación al juego agar.io
El juego se basa en el movimiento de bolas, donde encontraremos 3 tipos de bolas, "Comida" (Verde), "Enemigos" (Cambian de color) y "Jugador" (Rojo).
Jugador (Rojo): Se representa con una bola roja que inicia con un radio de 4px lo cual permite subsistir sin "comer" a 2 golpes, la idea es colisionar con la "Comida" que son bolas de color verdes que están quietas y aparecen aleatoriamente sobre el escenario cada vez que son comidas.
Comida (Verde): Al se colisionada por el jugador cambiará de posición aleatoriamente y sumará tamaño "Fuerza" y puntos al jugador.
Enemigos (Color Random): Los enemigos al collicionar con le "Jugador" debilitan y lo "adelgazan" así como van quitando puntos, adicionalmente cada vez que colisionan con el jugador a veces rebotan y aumentan de velocidad, como a veces lo consumen totalmente (Truco oculto).

La idea es mantenerse vivo en el juego los 30 segundos que dura el cronometro y hacer la mayor cantidad de puntos posibles.

## Explicación general del Código e imagen de contexto
Las clases que se muestran en el gráfico estan distribuidas en un archivo js diferente. La clase que reune más información en líneas de código es game porque esta implementa los diversos patrones para que funcione el juego. Según lo anterior, primero expondremos el código del archivo ejecutable y después todos los patrones para entender este Game.js: 
```
//Created Stage
var stageFrame = new Stage('canvas', 600, 400);
//Created Game
var  game1 = new Game(stageFrame);
game1.menu();
stageFrame.context.canvas.focus();

```
### Diagrama general de clases

![Diagrama Clases-JuegoComeCirculos](imagenes/DiagramaClasesJuegoPython-DiagramaFinal.png)
