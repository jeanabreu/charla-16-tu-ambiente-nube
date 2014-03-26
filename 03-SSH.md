##Servidor de SSH web

Ya que tenemos nuestro IDE ahora falta tener una consola SSH via web
para esos momentos donde no podemos hacer una conexión con un cliente
local, por ejemplo cuando estan detras de un firewall corporativo.

He visto varios paquetes para hacer esto, pero el que mejor me ha
funcionado es [Shell in a Box](https://code.google.com/p/shellinabox/).

#####Actualizar
    apt-get update && apt-get upgrade

#####Bajar el paquete

    wget http://archive.ubuntu.com/ubuntu/pool/universe/s/shellinabox/shellinabox_2.14-1_amd64.deb
    sudo dpkg -i shellinabox_2.14-1_amd64.deb

#####Configurar opciones adicionales
Vamos a editar el archivo de configuración

    sudo nano /etc/default/shellinabox

Luego encuentre esta linea y debe quedar asi:

    SHELLINABOX_ARGS="--no-beep --service=/:SSH -t"

Para reiniciar el servicio:

    sudo service shellinabox reload

Ya debe poder acceder utilizando la IP/dominio al puerto 4200
