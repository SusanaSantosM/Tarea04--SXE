# Tarea04--SXE

## 1. Utiliza la imagen de Ubuntu tag 22 y apoyandote en esta guía sigue sus instrucciones para instalar LAMP en dicho contenedor.

### Descargamos la imagen Ubuntu en docker
Instalamos la imagen de Ubuntu con la ultima versión con el comando:

``docker pull ubuntu``

![punto1.1](Imagen1_1.png)

### Instalamos LAMP en un contenedor con la iamgen Ubuntu
Creamos un contenedor con la imagen de Ubuntu:

``docker run -d --name ubuntucontenedor ubuntu tail -f /dev/null``

![punto1.2](Imagen1_2.png)

Luego accedemos a la terminal del contenedor **ubuntucontenedor** que hemos creado de la imagen Ubuntu:

``docker exec -it ubuntucontenedor bash``

En la terminal vamos a descargar el apache2 en el contenedor **ubuntucontenedor** :

``apt update``

``apt install -y apache2 apache2-utils``

Luego descargamos mariadb en el **ubuntucontenedor**:

 ``apt install -y mariadb-server mariadb-client``

Luego instalamos mysql con el siguiente comando:

``mysql_secure_installation``


> [!IMPORTANT]
> Cuando instalemos mysql nos va a pedir la contraseña del root, pero al no conocerlo tenemos  que salir de esa operación con Ctrl+C y luego ejecutar mariadb.

![punto1.3](Imagen1_3.png)

Comando para iniciarlizar mariadb:

``service mariadb start``

Luego volveremos a poner el comando ``mysql_secure_installation`` para instalarlo.

> [!CAUTION]
> Tendremos que seguir las instrucciones que apareceran de manera correcta para que el servidor se instale y no falle el root en el futuro.

![punto1.4](Imagen1_4.png)

Salimos de la consola del contenedor con ``exit``


## 2. Utiliza esta guía para instalar wordpress en el contenedor.


## 3. Comprueba que puedes acceder a wordpress. 
