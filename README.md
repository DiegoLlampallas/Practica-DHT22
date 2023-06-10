# Practica ESP32 con DHT11 de Diego Llampallas
Este repositorio muestra como podemos programar una ESP32 con el sensor DHT11.

## Introducción
A través de la página https://wokwi.com/  se puede hacer simulaciones de programas con arduino y sensores.
### Descripción

La ```Esp32``` la utilizamos en un entorno de adquision de datos, lo cual en esta practica ocuparemos un sensor (```DTH11```) para adquirir temperatura y humedad del entorno; Cabe aclarar que esta practica se usara un simulador llamado [WOKWI](https://https://wokwi.com/).


## Material Necesario

Para realizar esta practica se usaran los siguientes elementos:

- [WOKWI](https://https://wokwi.com/)
- Tarjeta ESP 32
- Sensor DHT11



## Instrucciones

### Requisitos previos

Para poder usar este repositorio necesitas entrar a la plataforma [WOKWI](https://https://wokwi.com/).


### Instrucciones de preparación de entorno 
1. Una vez dentro de wokwi seleccionar la tarjeta ESP32

![](https://github.com/DiegoLlampallas/Practica-DHT22/blob/main/6.png?raw=true)
2. Abrir la terminal de programación y colocar la siguente programación:

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
![](https://github.com/DiegoLlampallas/Practica-DHT22/blob/main/4.png?raw=true)
3. Instalar la libreria de **DHT sensor library for ESPx** como se muestra en la siguente imagen.

![](https://github.com/DiegoLlampallas/Practica-DHT22/blob/main/7.png?raw=true)

4. Hacer la conexion de **DHT11** con la **ESP32** como se muestra en la siguente imagen.

![](https://github.com/DiegoLlampallas/Practica-DHT22/blob/main/3.png?raw=true)

### Instrucciónes de operación

1. Iniciar simulador.
2. Visualizar los datos en el monitor serial.
3. Colocar la temperatura y humedad dando *doble click* al sensor **DHT11** 

## Resultados

Cuando haya funcionado, verás los valores dentro del monitor serial como se muestra en la siguente imagen.

![](https://github.com/DiegoLlampallas/Practica-DHT22/blob/main/5.png?raw=true)




## Evidencias

[Página](https://wokwi.com/projects/367114715905786881)


# Créditos

Desarrollado por Ing. Diego Alberto Llampallas Vega

- [GitHub](https://github.com/DiegoLlampallas)