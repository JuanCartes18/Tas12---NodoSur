# Nodo Sur - Infraestructura y Servicios 🌐

Este repositorio contiene la documentación y los archivos de configuración para la infraestructura del proyecto **Nodo Sur**. El entorno está desplegado sobre un clúster de **Proxmox** utilizando máquinas virtuales con **Ubuntu Server**.

## 🏗️ Arquitectura y Tecnologías

El proyecto simula un entorno de red y servicios web segmentados, implementando las siguientes tecnologías:
* **Virtualización:** Proxmox VE
* **Sistema Operativo:** Ubuntu Server
* **Redes:** Netplan (Configuración de interfaces y enrutamiento)
* **DNS:** BIND9 (Resolución de nombres y zonas locales)
* **Servidor Web:** Apache / Nginx (VirtualHosts para sitios)
* **Base de Datos:** MariaDB
* **Aplicación:** WordPress

## 📁 Contenido del Repositorio

* `/config`: Respaldo de los archivos de configuración clave (`/etc/bind`, `/etc/netplan`, `/etc/apache2/sites-available`, etc.).
* `/docs`: Documentación detallada sobre la topología de red, direccionamiento IP estático y guías de despliegue manual.
* `/scripts`: Scripts de automatización y mantenimiento del sistema.

## 🚀 Despliegue

Para replicar este entorno, se deben aprovisionar las máquinas virtuales en Proxmox y aplicar las configuraciones de red ubicadas en `/config/netplan`. Luego, iniciar los servicios en el siguiente orden:
1. Servidor DNS (BIND9)
2. Servidor de Base de Datos (MariaDB)
3. Servidores Web (Apache/Nginx)
