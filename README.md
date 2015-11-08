ionic-framework
=============================

![Ionic](http://ionicframework.com/img/ionic-logo-blue.svg)

Ionic-retailstore is a ready-to-go hybrid deveopment environment for building mobile apps with Ionic, Cordova, and Android. 
This is Docker image based on the Vagrant ionic-box (from [driftyco/ionic-box](https://github.com/driftyco/ionic-box)) to build the ionic-framework. 

Requirements
=================

* [Docker](https://www.docker.com/) 


Usage : ionic-retailstore
=================

    sudo docker run -it --rm --name ionic-retailstore -p 8100:8100 -p 35729:35729 dieple/ionic-retailstore

* App is running on http://$DOCKER_HOST:8100 which by default is [http://192.168.59.103/:8100](http://192.168.59.103/:8100)

If you have your own ionic sources, you can launch it with:

    sudo docker run -ti -p 8100:8100 -p 35729:35729 -v /path/to/your/ionic-project/:/myApp dieple/ionic-retailstore /bin/bash

Enable USB for the container

    sudo docker run -ti --rm -p 8100:8100 -p 35729:35729 --privileged -v /dev/bus/usb:/dev/bus/usb -v \$PWD:/myApp dieple/ionic-retailstore adb list

