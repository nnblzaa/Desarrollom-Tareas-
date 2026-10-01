# 🚗 Carro Solar ☀️️🤖

Proyecto de un vehículo autónomo/controlado alimentado por energía solar a través de paneles fotovoltaicos. Este repositorio contiene la documentación, diagramas, esquemáticos, enlaces a medios multimedia y el código fuente utilizado para la gestión de carga y control de motores.

---

## 📋 Descripción del Proyecto

El *Carro Solar* es un prototipo diseñado para demostrar la eficiencia y aplicación de las energías renovables en la movilidad eléctrica. Utiliza paneles solares para cargar una batería/supercapacitor y alimentar la electrónica de control y tracción.

### 🛠️ Componentes Principales
- *Controlador/Microcontrolador:* (Ej. Arduino UNO / ESP32 / Raspberry Pi Pico)
- *Panel Solar:* (Ej. Panel Solar 6V 2W / 12V 5W)
- *Módulo Carga/Regulador:* (Ej. TP4056 / Regulador Buck Boost LM2596)
- *Batería/Almacenamiento:* Li-ion 18650 3.7V / LiPo
- *Puente H / Driver de Motores:* L298N / L293D
- *Chasis y Motores:* Chasis 2WD/4WD con motorreductores DC

---

## 💻 Código Fuente

A continuación se muestra el código básico en C++ (Arduino) para el control del carro solar. Copia este código en tu IDE de preferencia:

```cpp
// ===============================================
// PROYECTO CARRO SOLAR - CÓDIGO DE CONTROL
// ===============================================

// Pines del Driver de Motores (Puente H)
const int IN1 = 5;
const int IN2 = 6;
const int IN3 = 9;
const int IN4 = 10;

// Pin de Monitoreo de Panel Solar (Opcional)
const int PIN_PANEL_SOLAR = A0;

void setup() {
  // Configuración de pines de motor como salida
  pinMode(IN1, OUTPUT);
  pinMode(IN2, OUTPUT);
  pinMode(IN3, OUTPUT);
  pinMode(IN4, OUTPUT);

  // Inicialización de la comunicación serial
  Serial.begin(9600);
  Serial.println("Iniciando Sistema de Carro Solar...");
}

void loop() {
  // Lectura del voltaje aproximado del panel solar
  int lecturaSolar = analogRead(PIN_PANEL_SOLAR);
  float voltajeSolar = lecturaSolar * (5.0 / 1023.0);
  
  Serial.print("Voltaje del Panel Solar: ");
  Serial.print(voltajeSolar);
  Serial.println(" V");

  // Rutina de movimiento de prueba
  moverAdelante();
  delay(3000);

  detener();
  delay(1000);

  moverAtras();
  delay(2000);

  detener();
  delay(2000);
}

// --- Funciones de Control de Motores ---

void moverAdelante() {
  digitalWrite(IN1, HIGH);
  digitalWrite(IN2, LOW);
  digitalWrite(IN3, HIGH);
  digitalWrite(IN4, LOW);
}

void moverAtras() {
  digitalWrite(IN1, LOW);
  digitalWrite(IN2, HIGH);
  digitalWrite(IN3, LOW);
  digitalWrite(IN4, HIGH);
}

void detener() {
  digitalWrite(IN1, LOW);
  digitalWrite(IN2, LOW);
  digitalWrite(IN3, LOW);
  digitalWrite(IN4, LOW);
}
