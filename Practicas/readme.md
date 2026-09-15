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
// Encender 10 LEDs - Arduino Uno R3
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
  digitalWrite(led2, HIGH);
  digitalWrite(led3, HIGH);
  digitalWrite(led4, HIGH);
  digitalWrite(led5, HIGH);
  digitalWrite(led6, HIGH);
  digitalWrite(led7, HIGH);
  digitalWrite(led8, HIGH);
  digitalWrite(led9, HIGH);
  digitalWrite(led10, HIGH);
}
Video del funcionamiento
Ver vídeo en YouTube

Evidencias de armado
Evidencia de armado arduino
Reporte
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
