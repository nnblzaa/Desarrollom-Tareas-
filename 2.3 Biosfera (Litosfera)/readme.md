## Nombre del proyecto
Biosfera (Litosfera)
## Descripción                                                                                                                            

La actividad consiste en construir un sistema de monitoreo de humedad del suelo mediante Arduino. El sensor se introduce en la tierra para medir su nivel de humedad y enviar una señal analógica al Arduino.

El programa instalado en el Arduino realiza la lectura del sensor mediante el pin analógico A0. De acuerdo con el valor obtenido, el sistema determina si el suelo se encuentra suficientemente húmedo o si está seco. Cuando se alcanza el nivel establecido como suelo seco, se utiliza un LED conectado al pin digital 13 como indicador.

Además, el programa permite visualizar las lecturas obtenidas mediante el Monitor Serie del Arduino IDE, facilitando la observación de los cambios de humedad en tiempo real.                                                     
## Objetivos de aprendizaje
* Comprender el funcionamiento de los sensores de humedad del suelo.
* Aprender a conectar un sensor analógico a un Arduino Uno.
* Aprender a utilizar las entradas analógicas y salidas digitales del Arduino.
* Programar Arduino para leer e interpretar datos de un sensor.
* Comprender cómo establecer un umbral de humedad para activar una respuesta.
* Controlar un LED mediante programación como indicador del estado del suelo.
* Utilizar el Monitor Serie para observar y analizar los datos obtenidos.
* Familiarizarse con el armado de circuitos en una protoboard.
* Relacionar la programación con una aplicación práctica de automatización y monitoreo, como el cuidado de plantas
## Resultados
[PDF](Litosfera/Resultados)

## Material y herramientas utilizadas
1. Arduino Uno
2. Sensor de humedad de suelo (sonda metálica + módulo sensor)
3. Protoboard
4. LED rojo
5. Resistencia para proteger el LED
6. Cables jumper macho-macho
7. Cable USB para conectar el Arduino a la computadora
8. Vaso/recipiente con tierra
9. Tierra o sustrato
10. Computadora portátil
11. Arduino IDE para programar y monitorear el sensor
## Imagen
<img width="1200" height="1600" alt="image" src="https://github.com/user-attachments/assets/e88632da-4ec0-4518-b92b-a693edbef230" />
<img width="1200" height="1600" alt="image" src="https://github.com/user-attachments/assets/33efd67c-e7c6-432b-b782-de257aaeb814" />

## Video
https://youtube.com/shorts/xpdc0fyvimA?si=_dpsDchNW70hRLil

## Codigo
[main.txt](./Codigo/main.txt)

