# 🤖 Proyecto Domotica

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
