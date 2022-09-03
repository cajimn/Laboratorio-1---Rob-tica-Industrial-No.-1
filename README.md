
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

Se diseña la pieza en Inventor que simula el tablero del laboratorio, para esto se creó una pieza de dimensiones 25 x 29 cm, con espesor de 1 cm. Además, se realiza la extrusión de 1 mm de las letras CIJ con esquinas redondeadas, esto para que las aceleraciones no sean tan grandes debido al cambio abrupto de dirección si se tienen esquinas de 90° y más si se tienen valores de definición 'z' muy pequeños. Con las letras se determinan luego en RobotStudio las rutas de las herramienta.

En RobotStudio se importa la pieza del tablero y se ubica en una posición acorde para que el robot pueda realizar el recorrido sin llegar a ninguna singularidad. Se ubica a 30° con respecto al eje x, a una distancia lo más parecida a la ubicación del tablero real en el laboratorio, en x y y positivos. Se define esta pieza como Work Object, definiendo el plano de trabajo por medio de 3 puntos en las esquinas del tablero, como se muestra a continuación.

![Captura](https://user-images.githubusercontent.com/51938754/188250642-cbe27416-ced9-46b4-9262-98f908d1a84d.PNG)

-------------------------------------------------------------
> ## Programa en RobotStudio

Para realizar el programa se realizaron los siguientes pasos:

  > - Se coloca el robot IRB 140 con su controlador y se hace invisible.
  > - Se coloca la herramienta creada que ya está almacenada en la biblioteca en la cabeza del robot.
  > - Se coloca como geometría el tablero, el cual debe ser un archivo de tipo SAT, este se hace girar respecto a x 30° y respecto a z 45°, además, se mueve a una posición en el cuadrante positivo del plano xy.
  > - Se crea el WorkObject y se coloca como punto de referencia el plano del tablero en la esquina inferior izquierda, esto se hace con el método de los 3 puntos.
  > - Se modifica la velocidad a v100 y la tolerancia a z10
  > - Se crean las trayectorias con rutas automáticas teniendo oprimida la tecla Shift sobre cada letra, para cada trayectoria se coloca como parámetro un valor de 100 como aproximación y partida de la trayectoria.
  
![Trayectorias](https://user-images.githubusercontent.com/52113892/188251412-194e57bc-c648-4e44-a915-232b9243e0f0.png)

  > - Se seleccionan todos los targets creados y se alinea la orientación del punto seleccionando en esta opción la herramienta diseñada y colocada en el robot.
  > - Se crea el Home con la opción de crear posición de ejes y se guarda como trayectoria.
  
![RS](https://user-images.githubusercontent.com/52113892/188251415-1aeab55e-7688-42c1-94da-47c25f12dfae.png)

  > - Sincronizamos el controlador y modificamos el código de RAPID en el archivo "main" para definir el orden en el que queremos que se ejecuten las trayectorias.
  
![Codigo rapid](https://user-images.githubusercontent.com/52113892/188251414-c7bed7b5-a3e3-4ac4-9164-d7d4081b840d.png)

  > - Guardamos el programa para colocarlo en la USB posteriormente
     

https://user-images.githubusercontent.com/52113892/188251400-23d41d0e-00c9-4046-b221-1e50c5040ecb.mp4


--------------------------------------------------------------

> ## Implementación en LabSIR


https://user-images.githubusercontent.com/68668422/188003012-f34fde90-97bd-4622-82bc-f2a98e422880.mp4





https://user-images.githubusercontent.com/68668422/188003161-35d4e27c-c4d0-4c2c-be0b-8775f0c77d8f.mp4

