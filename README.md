# Netdata + Alertmanager

Este repositorio contiene la configuración para desplegar **Netdata** y **Alertmanager** utilizando Docker Compose, permitiendo la monitorización y alertas de sistemas en tiempo real.

## 📋 Contenido del repositorio

- **docker-compose.yml** – Archivo para desplegar los servicios de Netdata y Alertmanager.
- **alertmanager/** – Carpeta con la configuración de Alertmanager.
- **README.md** – Documentación del proyecto.

## 🚀 Instalación

Sigue estos pasos para desplegar el stack en tu servidor:

1. **Clonar el repositorio:**

   ```bash
   git clone https://github.com/mariaortiz02/Netdata-alertmanager.git
   cd Netdata-alertmanager
2. **Levantar los servicios con Docker Compose:**

   ```bash
   docker-compose up -d

3. **Verificar los contenedores en ejecución:**

   ```bash
   docker ps

## 📡 Servicios disponibles
Netdata Dashboard: http://localhost:19999
Alertmanager UI: http://localhost:9093

## ⚙️ Configuración
**Netdata:** La configuración de Netdata se encuentra en el archivo docker-compose.yml. Puedes personalizar el volumen de datos y los parámetros de arranque.
**Alertmanager:** Edita la configuración de Alertmanager en alertmanager/config.yml para personalizar las reglas de alerta.
Ejemplo de notificación a Slack:
 ```bash
route:
  receiver: 'slack'
receivers:
  - name: 'slack'
    slack_configs:
      - channel: '#alertas'
        send_resolved: true
        api_url: 'https://hooks.slack.com/services/TOKEN'



