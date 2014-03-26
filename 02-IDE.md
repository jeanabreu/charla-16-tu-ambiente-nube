##Montando Cloud9

Ahora que tenemos nuestro VPS listo vamos a montar un IDE para poder trabajar
desde nuestro browser. Para esto vamos a usar la versión open source de
[Cloud 9](https://github.com/ajaxorg/cloud9).

Primero vamos a resolver el tema de los requisitos previos:

#####NodeJS & NPM

    sudo apt-get install software-properties-common
    sudo apt-get install python-software-properties python g++ make
    sudo add-apt-repository ppa:chris-lea/node.js
    sudo apt-get update
    sudo apt-get install nodejs

#####Clonar Cloud9

Ahora vamos a clonar desde github la ultima versión del IDE de Cloud9, vamos
para dejarlo organizado pueden crear un directorio y colocarlo ahi.

    mkdir Code
    cd Code

    git clone https://github.com/ajaxorg/cloud9.git
    cd cloud9
    npm install

#####Ejecutarlo
Estando en el directorio donde hicimos el clone de Cloud9 podemos ejecutarlo con:

    bin/cloud9.sh -w ~/Code -l 0.0.0.0 --username smirnoff --password ice
