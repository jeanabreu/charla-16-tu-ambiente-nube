##Configuración inicial

#####Actualizar los repositorios

    sudo-apt-get update

#####Instalar CURL y GIT

    sudo apt-get install curl
    sudo apt-get install git

#####Instalar RVM

    \curl -L https://get.rvm.io | bash -s stable
    source /usr/local/rvm/src/rvm/scripts/rvm
    rvm requirements

#####Seguimos ahora con Ruby

    rvm install ruby
    rvm use ruby --default
    rvm rubygems current

#####Para probrar que todo este instalado correctamente vamos a monstar Rails

    gem install rails
