# FTP

- Tenemos una cuenta en ftp.drivehq.com
	usuario: amoksito
	pass: Coquito1

- ncftpput -R -v -u "amoksito" ftp.drivehq.com /Draft /home/emiliano/Dropbox/Draft
	Con esto subimos una carpeta entera.

- prompt: Desactiva la Shell interactiva, así no tenemos que apretar 'y' todo el tiempo.

# GIT

- Más útil que FTP es GIT hoy en día. Tenemos un repositorio propio: amoksito/personal.
- git clone https://github.com/amoksito/personal
- git commit -m "nuevo"
- git push -u origin master

# Linux

- En Arch instalar: gvfs-google y gvfs-goa installed para Google Drive.

- Bash-Completion para que funque tab en la consola.

- Reiniciar Shell:  Alt + F2, type "r" then Enter.

- libsoup32 parece arreglar el error de HTTP unauthorized.

- Mailnag para tener buenas notificaciones de mail.

- Seahorse: para administrar las contraseñas.

# Bash

- Autojump. 
	- Necesitamos "sourcearlo": source /etc/profile.d/autojump.bash. 
	- Para que esto sea permanente, agregamos: . /usr/share/autojump/autojump.bash
	- Luego saltamos a cualquier directorio al que ya hayamos accedido con j, y podemos autocompletar con TAB.
	- También podemos usar 'jo' para abrir una carpeta en Nautilus.

- Al bashrc se le pueden agregar cosas como "date & uptime -p"

- Shopt permite varias opciones para Bash. Algunas utiles:

	- shopt -s checkwinsize: cambia el tamaño del Bash si fuese necesario. 
	- shopt -s cdspell: pequeños errores de tipeo son arreglados automáticamente.
	- shopt -s autocd: no hace falta escribir 'cd', basta con el nombre del directorio.

- Colores

BLACK="\033[30m"
RED="\033[31m"
GREEN="\033[32m"
YELLOW="\033[33m"
BLUE="\033[34m"
PINK="\033[35m"
CYAN="\033[36m"
WHITE="\033[37m"
NORMAL="\033[0;39m"

	- Los colores se usan con "echo" de esta manera: echo -e $GREEN "Hi, today is $(date)" $NORMAL
	- También podemos agregar algún ascii art, simplemente lo bajamos, y con cat art lo tenemos. 

- También podemos probar instalando archey. 
- 

# Sublime

- Necesario tanto texlive como telive-extra.
- Se le pueden pasar instrucciones a Pandoc en el YAML, ejemplo:

---
title: Ética en Husserl
author: Emiliano Sesarego
geometry: margin=3cm
---

- Para tener soporte unicode en Sublime agregar esto al archivo de configuración de PANDOC.

"PDF TeTeX TOC": {
        "scope": {
          "text.html": "html",
          "text.html.markdown": "markdown",
          },
        "pandoc-arguments": [
          "-s", "--toc", "--number-sections", "--parse-raw", "--latex-engine=xelatex",
          "-t", "pdf",
         ],
      },

- Con el paquete "Pandoc" podemos convertir con Ctrl + Shift + P, pero también podemos construir un __Build System__ y luego simplemente apretar __F7__.
- Tambien podemos usar __PANDOWN__ y generar ePub automáticamente.
- Colores: predawn.

# Alias

- alias lll='ls -Ah --group-directories-first'

- comandos con los que utilizar el copyboard: 

alias pbcopy='xsel --clipboard --input'
alias pbpaste='xsel --clipboard --output'


# Paquetes para ARCH

- xorg-xkill