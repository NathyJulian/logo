# Manual de instalacion
<!--<h1>Manual de instalacion</h1> -->
Este manual proporciona instrucciones detalladas para instalar y configurar el sistema FacturadorPro3 en un entorno Linux utilizando Valet. Asegúrese de seguir cada paso cuidadosamente para garantizar una instalación exitosa.

## Requisitos Previos

- Asegúrate de tener acceso root.
- Instala PHP 7.2 y todas las librerías requeridas por
- el aplicativo y Laravel.
- Instala MySQL (y PhpMyAdmin opcional) para las pruebas de la base de datos.
- Instala Git, Curl, Composer.

### Pasos

#### 1.Instalación de PHP 7.2 en Ubuntu
Ubuntu no cuenta con la versión 7.2 de php de manera nativa por lo que se debe seguir un par de pasos para agregar un repositorio y luego proceder con la instalación, ellos son:

a. Para poder ejecutar los siguientes comandos debe acceder a la terminal como usuario root.
~~~
apt-get update
~~~
b. Para poder agregar un PPA, ejecute los siguientes:
~~~
apt-get install software-properties-common
apt-get install python-software-properties
~~~
c. Para agregar el PPA, en algunos casos solicitará confirmar con enter
~~~
add-apt-repository ppa:ondrej/php
apt-get update
~~~
d. Procedemos a Instalar PHP, aunque se instalar algunas librerías junto con PHP, se agregan para asegurar la instalación
~~~
apt-get install php7.2 php7.2-mbstring php7.2-soap php7.2-zip php7.2-mysql php7.2-curl php7.2-gd php7.2-xml php7.2-mcrypt
~~~
#### 2. Instalación de MySQL y PhpMyAdmin

Instalamos Mysql, phpmyadmin opcional
~~~
apt-get install mysql-server-5.7 mysql-client-5.7 phpmyadmin.
~~~
- Se le solicitara contraseña dos veces, con su confirmación, tanto para mysql como para phpmyadmin

#### 3. Instalación de Curl y Git
Instalamos Curl y Git
~~~
apt-get install git
apt-get install curl
~~~
#### 4.Instalación de Composer
Luego se procede a instalar Composer
~~~
apt-get install composer
~~~
Dar permisos de lectura y escritura a la carpeta composer
~~~
Chmod –R 777 ~/.composer
~~~
#### 5.Instalación de librerías de Valet
Instalar librerias cpriego de Valet
~~~
composer global require cpriego/valet-linux
~~~