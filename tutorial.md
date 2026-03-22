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
