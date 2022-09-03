
<h1 align="center"> Laboratorio 1 Robótica industrial </h1>

## Universidad Nacional de Colombia
-------------------------------------------------------------
> ## Autores

  > - Carlos Mario Jiménez Novoa. [cajimn](https://github.com/cajimn)
  > - Ivanna Lisette Medina Cruz. [IvannaMedinac](https://github.com/IvannaMedinaC)
  > - Juan Sebastian Rangel Araque. [juanBananin](https://github.com/juanBananin)


## Procedimiento

> ## Diseño de la herramienta

Para el diseño de la herramiento en Robot estudio se optó por usar los elementos de creación de solidos de esta aplicación, se generó una base cilíndirca con el mismo diámetro del plato y una altura de un centimetro, un cilindro con menor diámetro y  con altura de 10 cm y un cono con una altura de 2 cm como se ve en la imagén a continuación.

![Herramienta](https://user-images.githubusercontent.com/52113892/188249137-9250b171-d017-44f4-8832-530f6c0c9a62.png)
 
Luego de esto, se gener´´o el TCP correspondiente en la punta de la herramienta.

Para la implementación en la vida real, se realizó la impresión 3D de un portaherramientas capaz de acoplarse al plato del robot y que pueda sostener el marcador:

![Portaherramientas](https://user-images.githubusercontent.com/52113892/188249309-d4fd0d2c-51ed-45fa-a4d4-61c64faebfd3.png)

Este tendría implementado unos tornillos M3 en los huecos laterales para que el marcador no se pudiese desplazar en esas direcciones y en la parte del fondo del agujero, un resorte que iría pegado a la base y al marcador que permita un pequeño amoritguamiento del marcador al entrar en contacto con el tablero. El resultado final fue:

![herramientaReal](https://user-images.githubusercontent.com/52113892/188249469-ecbbfa11-b053-4c7c-aae5-30acc4c6a9a0.png)

-------------------------------------------------------------
> ## Diseño del tablero

La base del juego fue el uso de bitwise para crear las figuras y verificar las colisiones, lo cual fue un método que agilizó la funcionalidad del tetris, además, el juego cuenta con un menú donde elegiras tu número de minos y el tipo de figura con el que quieres jugar, el juego contiene unos marcadores con los cuales podrás medir tu habilidad del juego, implementando niveles de acuerdo al puntaje que vayas adquiriendo, el cual qumenta la velocidad de caida del tetromino. Dichos marcadores quedaran guardados en un JSON, esto te permitirá ir mejorando tus puntajes cada vez que juegues. 

-------------------------------------------------------------
> ## Programa en RobotStudio

--------------------------------------------------------------



https://user-images.githubusercontent.com/68668422/188003012-f34fde90-97bd-4622-82bc-f2a98e422880.mp4





https://user-images.githubusercontent.com/68668422/188003161-35d4e27c-c4d0-4c2c-be0b-8775f0c77d8f.mp4

