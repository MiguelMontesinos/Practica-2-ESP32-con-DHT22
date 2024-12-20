# Practica-2-ESP32-con-DHT22


Programamos una ESP32 con el sensor DHT 22

## Introducción
## Descripción

En esta práctica ocuparemos un sensor (DTH 22) para obtener la humedad y temperatura a nuestro alrededor y utilizaremos la Esp32 para adquirir los datos y utilizaremos WOKWI para la simulación.

## Material a utilizar
- Sensor DHT22
- Tarjeta ESP32
- wokwi.com

## Instrucciones
## Pre Requerimientos
Utilizar la plataforma Wokwi
## Instrucciones de preparación 
1.- Abrir la terminal de programación y escribir un código como el siguiente
```
#include "DHTesp.h"


const int DHT_PIN = 15;
DHTesp dhtSensor;


void setup() {

  Serial.begin(115200);
  dhtSensor.setup(DHT_PIN, DHTesp::DHT22);
}

void loop() {

  TempAndHumidity  data = dhtSensor.getTempAndHumidity();
  Serial.println("Temp: " + String(data.temperature, 1) + "°C");
  Serial.println("Humidity: " + String(data.humidity, 1) + "%");
  Serial.println("---");
  delay(1000);
}
```
2.- Insertar la librería del sensor DHT22 para nuestra tarjeta DHT22

![image](https://github.com/MiguelMontesinos/Practica-2-ESP32-con-DHT22/blob/main/393537542-32b41991-e97a-4cb5-afa2-b0fcd211e35b.png?raw=true)

3.- Conectar la DHT22 con la ESP32, con el GND, el puerto 15 y la salida de 3V

![image](https://github.com/MiguelMontesinos/Practica-2-ESP32-con-DHT22/blob/main/393537602-6f660f6b-c489-4985-8581-e2748aa7149d.png?raw=true)

## Instrucciones de operación 
1.- Iniciar el Simulador
2.- Visualizar la obtención de los datos en el monitor serial
3.- Obtener la temperatura y la humedad dando click dos veces a nuestro sensor DHT22

## Resultados
Los valores se veran como en la siguiente imagen:

![image](https://github.com/MiguelMontesinos/Practica-2-ESP32-con-DHT22/blob/main/393537602-6f660f6b-c489-4985-8581-e2748aa7149d.png?raw=true)

# Créditos
Desarrollado por Ing. Montesinos Molina Miguel de Jesus

[GitHub](https://github.com/MiguelMontesinos).
