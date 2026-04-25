TP Integrador — Computación Aplicada
Universidad de Palermo · Facultad de Ingeniería
Licenciatura en Ciberseguridad · 2026

Descripción
Trabajo Práctico Integrador Grupal de la materia Computación Aplicada (0306).
El trabajo consiste en la configuración de un servidor GNU/Linux Debian con los siguientes servicios: SSH, Apache con PHP, MariaDB, configuración de red estática, gestión de almacenamiento con particiones y un sistema de backup automatizado mediante scripts y cron.

Integrantes
NombreHerman CesarLuciana FierroRoberto MastromaureOmar Jeremias Palacios Toconas

Estructura del repositorio
/
├── root.tar.gz          # Directorio /root
├── etc.tar.gz           # Directorio /etc
├── opt.tar.gz           # Directorio /opt
├── www_dir.tar.gz       # Directorio /www_dir
├── backup_dir.tar.gz    # Directorio /backup_dir
└── var/                 # Directorio /var (splitteado en partes)

Resumen de tareas realizadas
1. Configuración del entorno

Blanqueo y cambio de contraseña de root
Configuración del hostname como TPServer

2. Servicios

Actualización del SO a Debian 12
Instalación y configuración de SSH con autenticación por clave pública/privada
Instalación y configuración de Apache con soporte PHP (v7.3+)
Instalación y configuración de MariaDB con carga del script db.sql

3. Configuración de red

IP estática configurada en /etc/network/interfaces
Campos configurados: ADDRESS, NETMASK, GATEWAY

4. Almacenamiento

Disco adicional de 10 GB agregado a la VM
Dos particiones tipo 83:

/www_dir → 3 GB
/backup_dir → 6 GB


Montaje automático configurado en /etc/fstab
Archivo particion generado en /opt con contenido de /proc/partitions

5. Backup

Script backup_full.sh desarrollado y guardado en /opt/scripts
Backups con nombre en formato YYYYMMDD
Argumentos: origen y destino
Opción -help incluida
Validación de sistemas de archivos disponibles
Tareas automatizadas con cron:

Todos los días a las 00:00 hs → backup de /var/logs
Lunes, Miércoles y Viernes a las 23:00 hs → backup de /www_dir




Tecnologías utilizadas

GNU/Linux Debian 12
Apache2 + PHP
MariaDB
OpenSSH
Bash scripting
Cron
Oracle VirtualBox
