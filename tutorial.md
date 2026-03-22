# Tutorial de Git y Linux

Este documento recopila los comandos que voy ejecutando en Debian 13, junto con una explicación de su propósito. La idea es usarlo como guía de repaso.

---

## 1. Instalación de Git

- `sudo apt update`  
  Actualiza la lista de paquetes disponibles en los repositorios.

- `sudo apt install git -y`  
  Instala Git en el sistema. El parámetro `-y` acepta automáticamente la confirmación.

- `git --version`  
  Verifica la versión instalada de Git.

---

## 2. Configuración inicial de Git

- `git config --global user.name "Tu Nombre"`  
  Define el nombre que aparecerá en los commits.

- `git config --global user.email "tuemail@example.com"`  
  Define el correo asociado a los commits.

---

## 3. Crear un repositorio local

- `mkdir practica-git`  
  Crea una carpeta para el proyecto.

- `cd practica-git`  
  Entra en la carpeta.

- `git init`  
  Inicializa un repositorio Git en la carpeta.

---

## 4. Primer archivo y commit

- `nano tutorial.md`  
  Crea un archivo de documentación en formato Markdown.

- `git add tutorial.md`  
  Añade el archivo al área de preparación (*staging*).

- `git commit -m "Primer commit: inicio del tutorial"`  
  Registra el primer commit con un mensaje descriptivo.

---

## 5. Conectar con GitHub

- `git remote add origin https://github.com/TU-USUARIO/tutorial-git-linux.git`  
  Enlaza el repositorio local con el remoto en GitHub.

- `git push -u origin master`  
  Sube los cambios al repositorio remoto.  
  *(En algunos casos la rama principal se llama `main` en lugar de `master`.)*

## 6. Instalación de KVM y Virt-Manager

- `sudo apt install qemu-kvm libvirt-daemon-system libvirt-clients bridge-utils virt-manager -y`  
  Instala el motor de virtualización y herramientas de gestión.

- `sudo usermod -aG libvirt $(whoami)`  
  Agrega el usuario al grupo libvirt para administrar VMs sin sudo.

- Distribución elegida para Zabbix: **Ubuntu Server Minimal 22.04**  
  Ligera, estable y con soporte oficial de Zabbix.

## 8. Conexión SSH entre host y VM

- `sudo apt install openssh-server -y`: Instala el servidor SSH en la VM.
- `systemctl enable ssh && systemctl start ssh`: Habilita y arranca el servicio SSH.
- `ip a`: Muestra la dirección IP de la VM.
- `ssh usuario@IP_VM`: Conecta desde el host a la VM vía SSH.

