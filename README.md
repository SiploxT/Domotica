# 🤖 Proyecto Domotica

![maqueta24](https://github.com/SiploxT/Domotica/assets/102182731/b27580cb-5b0d-42b8-b559-d7470549808e)
![EsquemaConexiones](file:///home/a22joelmz/Descargas/EsquemaConexions_bb(1).svg)

## 📄 Pasos previos

Antes de comenzar el proyecto, es necesario preparar nuestro SO (Sistema Operativo) para instalarlo en el equipo que utilice nuestro servidor:

- Instalar el SO desde: https://www.raspberrypi.com/software/raspberry-pi-desktop/
- Crear el USB de instalación con el uso de: https://etcher.balena.io/
- Insertar el USB en nuestro equipo de servidor para instalar el SO descargado anteriormente.

Tras esto, debemos instalar y configurar Node-Red y Mosquitto con los siguientes comandos:

· **Node-Red**
- apt install bash
- bash <(curl -sL https://raw.githubusercontent.com/node-red/linux-installers/master/deb/update-nodejs-and-nodered)
- sudo systemctl enable nodered.service

· **Mosquitto**
- sudo apt update
- sudo apt upgrade
- sudo apt-get install mosquitto mosquitto-clients
- sudo systemctl enable mosquitto.service (Esto lo haremos para iniciar Mosquitto tras haberlo instalado)

## 📄 Detalles de Actividades

### P1: Conexión ESP32 a servidor MQTT

En esta práctica, debemos conectar el ESP32 a el servidor MQTT, y a través del código de la práctica, comprobar el funcionamiento.<br/>
El resultado debería ser este:

![MQTTConexión](https://github.com/SiploxT/Domotica/assets/102182731/e75a2a01-2a71-4465-959c-adeadcf73bfe)

### P2: Control de un LED

Debemos conseguir controlar un LED a través de el código de la P2, Node-Red y Arduino.<br/>
Con la ayuda de esta imagen, podremos entender las conexiones y el flujo de esta practica:

![ControlLED](https://github.com/SiploxT/Domotica/assets/102182731/e4bafb8e-3cb9-4876-9fbc-59138fd37191)

### P3: Utilización de un botón

Realizaremos la misma actividad de controlar un LED, pero esta vez con un pulsador que nos facilitará la tarea.<br/>
De la misma manera, aquí tenemos la conexión y el flujo:

![BotonLED](https://github.com/SiploxT/Domotica/assets/102182731/241f65c8-5880-4ba1-be6a-ea57fd4031e5)

### P4: DHT11

Utilizaremos el DHT11, un sensor de temperatura, para averiguar la temperatura de cualquier ambiente que queramos y enviarla a el propio servidor.<br/>
En este caso el flujo es algo más complicado, pero funciona de igual manera que los otros:

![FlujoDHT11](https://github.com/SiploxT/Domotica/assets/102182731/d393ca55-e386-4b07-8360-3d20610bd289)
