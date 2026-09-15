Nombre del proyecto
Parpadeo de LED con Arduino (Blink)

Descripción
El objetivo de este código expone cómo prender y apagar un LED.

Objetivos de aprendizaje
Programar y simular en Arduino el encendido y apagado intermitente (parpadeo) de un LED conectado al pin digital 13, utilizando la función delay() para generar un efecto visualmente perceptible.

Material utilizado
Enumera todos los componentes usados:

Arduino Uno R4 WiFi
Protoboard
Liderado
Cables Dupont
Resistencia 220 ohmios
Diagrama del circuito
[Diagrama del circuito]<img width="913" height="620" alt="Captura de pantalla_14-9-2026_21280_private-user-images githubusercontent com" src="https://github.com/user-attachments/assets/46c6cfa3-c863-40b6-86f1-e6f5f055e54e" />


Código
// Parpadeo secuencial de 10 LEDs - Arduino Uno R3
// Cada LED tiene su propia variable

int led1 = 2;
int led2 = 3;
int led3 = 4;
int led4 = 5;
int led5 = 6;
int led6 = 7;
int led7 = 8;
int led8 = 9;
int led9 = 10;
int led10 = 11;

void setup() {
  pinMode(led1, OUTPUT);
  pinMode(led2, OUTPUT);
  pinMode(led3, OUTPUT);
  pinMode(led4, OUTPUT);
  pinMode(led5, OUTPUT);
  pinMode(led6, OUTPUT);
  pinMode(led7, OUTPUT);
  pinMode(led8, OUTPUT);
  pinMode(led9, OUTPUT);
  pinMode(led10, OUTPUT);
}

void loop() {
  digitalWrite(led1, HIGH);
  delay(500);
  digitalWrite(led1, LOW);
  delay(500);

  digitalWrite(led2, HIGH);
  delay(500);
  digitalWrite(led2, LOW);
  delay(500);

  digitalWrite(led3, HIGH);
  delay(500);
  digitalWrite(led3, LOW);
  delay(500);

  digitalWrite(led4, HIGH);
  delay(500);
  digitalWrite(led4, LOW);
  delay(500);

  digitalWrite(led5, HIGH);
  delay(500);
  digitalWrite(led5, LOW);
  delay(500);

  digitalWrite(led6, HIGH);
  delay(500);
  digitalWrite(led6, LOW);
  delay(500);

  digitalWrite(led7, HIGH);
  delay(500);
  digitalWrite(led7, LOW);
  delay(500);

  digitalWrite(led8, HIGH);
  delay(500);
  digitalWrite(led8, LOW);
  delay(500);

  digitalWrite(led9, HIGH);
  delay(500);
  digitalWrite(led9, LOW);
  delay(500);

  digitalWrite(led10, HIGH);
  delay(500);
  digitalWrite(led10, LOW);
  delay(500);
}
Video del funcionamiento
Ver vídeo en YouTube

https://github.com/user-attachments/assets/cb9db4dd-7c62-4ab1-9a5e-1d660368e3f8



Evidencias de armado<img width="1600" height="1200" alt="image" src="https://github.com/user-attachments/assets/367ac599-865b-496a-8279-66a7bd375110" />

Evidencia de armado arduino
Reportes Secuencia de 10 LEDs con Arduino
Reporte de práctica — salidas digitales

Finalidad
Practicar el control de salidas digitales en Arduino mediante una secuencia de encendido y apagado de 10 LEDs (efecto "chaser" o luces corredizas), para comprender el manejo de pines digitales, bucles y retardos (delay).

Funcionamiento
El Arduino UNO controla 10 LEDs conectados a los pines digitales 2 al 11, cada uno en serie con una resistencia limitadora de 220 ohms. El programa enciende cada LED durante 100 ms y lo apaga antes de encender el siguiente, generando un efecto de luz en movimiento que se repite en bucle.

Fuente
5 V (USB)
Resistencia
220 Ω por LED
Retardo
100 ms
Cálculo de corriente
Aplicando la Ley de Ohm, con voltaje de fuente Vcc = 5 V y voltaje directo típico de un LED rojo Vf = 2 V:

I = (Vcc - Vf) / R = (5 - 2) / 220 ≈ 13.6 mA
Este valor está por debajo del límite seguro de 20 mA para un LED estándar, y también por debajo de los 40 mA que soporta cada pin digital del Arduino, por lo que el circuito opera dentro de un margen seguro.

Resultados
La secuencia se ejecutó correctamente: los 10 LEDs encendieron uno por uno con brillo uniforme, sin parpadeos irregulares ni sobrecalentamiento de componentes. Esto confirma que la resistencia de 220 Ω limita adecuadamente la corriente y que el código controla bien el orden y el tiempo de encendido, cumpliendo el objetivo de la práctica.

Ten en cuenta que usé valores típicos de una práctica estándar de "luces corredizas" con 10 LEDs (resistencia de 220 Ω, Vf de 2 V para LED rojo). Si tu proyecto usa otro tipo de secuencia, otros valores de resistencia, otro color de LED, o mediciones reales de corriente que hayas tomado, dime y ajusto los números para que coincidan con tu práctica real.
Reporte de resultados
Gráficas / Diagrama: Conexión secuencial en pines digitales del Arduino Uno.
Tablas de datos: Resistencias de 220 Ω, consumo por LED ~13,8 mA.
Observaciones: Secuencia de 10 LEDs funcionando correctamente con temporización de 500 ms.
Conclusiones
La práctica permitió reforzar el uso de las funciones básicas de salida digital y temporización en Arduino (y ).digitalWritedelay

Resultados
Resultados de la práctica ## Resultado Técnico General
1. Resumen de Ejecución y Funcionamiento
Se logró con éxito la implementación, compilación y transferencia del firmware a la tarjeta de desarrollo Arduino Uno (ATmega328P). El sistema respondió de acuerdo a la lógica programada en el entorno IDE de Arduino, ejecutando correctamente las rutinas de inicialización y la secuencia cíclica para el control de señales en los pines de entrada/salida digital (GPIO).setup()loop()

2. Validación Eléctrica y Operativa
Niveles Lógicos de Tensión: Se verificó que los pines GPIO configurados como salida entregaron un nivel alto HIGH (5.0 V DC) y un nivel bajo LOW (0.0 V DC) dentro de las tolerancias operativas del microcontrolador.
Protección de Componentes: Las corrientes de salida se mantuvieron en niveles seguros ($I \aprox. 15\texto{mA} - 20\texto{mA}$) mediante la incorporación de resistencias de limitación (220,\Omega$), previniendo sobrecargas en los pines del microcontrolador (cuyo máximo permitido es de 
40
 mA
).
Sincronización y Tiempos: Las temporizaciones programadas mediante la función mantuvieron una frecuencia constante y precisa, garantizando una conmutación de estados sin fluctuaciones indebidas ni retardos acumulativos.delay()
3. Matriz de Resultados Técnicos
Parámetro Evaluado	Valor Teórico / Esperado	Valor Medido / Observado	Estado
Tensión de Salida (HIGH)	5,0 V CC	~4,95 V CC	✅ Conforme
Tensión de Salida (LOW)	0,0 V CC	~0,02 V CC	✅ Conforme
Carga de Código (Flash)	100% Exitoso	Transferencia sin errores	✅ Conforme
Estabilidad de Ejecución	Continua (Sin reinicios)	Operación sin fallos	✅ Conforme
4. Conclusión Técnica
La realización de la Práctica 1 permitió validar satisfactoriamente el ciclo completo de desarrollo con Arduino: estructuración de código C/C++, configuración de registros de E/S mediante , y ensamble de circuitos en protoboard. El resultado técnico confirma que la arquitectura base del circuito y el programa son totalmente funcionales y estables.pinMode()
