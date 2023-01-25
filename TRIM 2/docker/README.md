# Docker - Christian Moreno #

## 1.2 Primera prueba ##

  · Instalamos docker
  
![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/docker/IMG/1.png)

  · Comprobamos que el usuario está en el grupo docker.
![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/docker/IMG/2.png)

  · Consultar el estado de IP_FORWARD. Debe estar activo=1
![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/docker/IMG/3.png)

  · Comprobamos que se muestra la información de las versiones cliente y servidor.
![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/docker/IMG/4.png)

  · Ejecutamos el siguiente comando:
  
![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/docker/IMG/5.png)

  · docker images, ahora vemos la nueva imagen "hello-world" descargada en nuestro equipo local.

  ·docker ps -a, vemos que hay un contenedor en estado 'Exited'.
  
  ·docker stop IDContainer, parar el conteneder identificado por su IDContainer. Este valor lo obtenemos tras consultar la salida del comando anterior (docker ps -a).

  ·docker rm IDContainer, eliminar el contenedor.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/docker/IMG/6.png)

# 2. Creación manual de nuestra imagen #

## 2.1 Crear un contenedor manualmente ##

  · docker pull debian, descargamos una imagen en local.
  
  · docker images, comprobamos que se ha descargado.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/docker/IMG/7.png)


## 2.2 Personalizar el contenedor ##

  · dento del contenedor actualizamos y descargamos nginx y el editor nano.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/docker/IMG/8.png)

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/docker/IMG/9.png)

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/docker/IMG/10.png)

  · Crear un fichero HTML holamundo1.html.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/docker/IMG/11.png)

  · Crear un script /root/server.sh con el siguiente contenido:

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/docker/IMG/12.png)

## 2.3 Crear una imagen a partir del contenedor ##

  · abrimos otra terminal y  partir del contenedor modificado vamos a crear la nueva imagen que se llamará "nombre-del-alumno/nginx1".
  
![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/docker/IMG/14.png)

  · Ahora podemos parar el contenedor, docker stop app1debian y
  
  · Eliminar el contenedor, docker rm app1debian.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/docker/IMG/15.png)

# 3 Crear contenedor a partir de nuestra nueva imagen #

## 3.1 Crear contenedor con Nginx ##

  ·  iniciar el contenedor a partir de la imagen anterior.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/docker/IMG/16.png)

## 3.2 Comprobamos ##

  · docker ps, nos muestra los contenedores en ejecución.
  
![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/docker/IMG/17.png)

  · Abrir navegador web y poner URL 0.0.0.0.:PORT

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/docker/IMG/18.png)

  · Comprobar el acceso al fichero HTML.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/docker/IMG/19.png)

  · Paramos el contenedor app2nginx1 y lo eliminamos.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/docker/IMG/20.png)

## 3.3 Migrar la imagen a otra máquina ##

### No realicé este punto ##

# 4 Dockerfile #

## 4.1 Preparar ficheros ##

  · Crear directorio /home/nombre-alumno/dockerXXlocal.
  
  · Entramos en el directorio:

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/docker/IMG/22.png)

  · Crear fichero holamundo2.html con el siguiente contenido:

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/docker/IMG/23.png)

  · Crear el fichero Dockerfile con el siguiente contenido:

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/docker/IMG/24.png)

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/docker/IMG/25.png)


## 4.2 Crear imagen a partir del Dockerfile ##

  · Docker build -t nombre-alumno/nginx2 ., construye una nueva imagen a partir del Dockerfile. 

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/docker/IMG/26.png)

  · Nos aparece nuestra nueva imagen:
  
![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/docker/IMG/27.png)

## 4.3 Crear contenedor y comprobar ##

  · A continuación vamos a crear un contenedor con el nombre app4nginx2

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/docker/IMG/28.png)

  · Desde otra terminal:

  · Docker ps, para comprobar que el contenedor está en ejecución y en escucha por el puerto deseado.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/docker/IMG/29.png)

  · Comprobar en el navegador:
  
  · URL http://localhost:PORTNUMBER

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/docker/IMG/30.png)

  · URL http://localhost:PORTNUMBER/holamundo2.html

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/docker/IMG/31.png)


## 4.4 Usar imágenes ya creadas. ##

  · Crea el directorio dockerXXweb. Entrar al directorio.

  · Crear fichero holamundo3.html con:

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/docker/IMG/32.png)

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/docker/IMG/33.png)

  · Crea el siguiente Dockerfile

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/docker/IMG/34.png)

  · crear la imagen.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/docker/IMG/35.png)

  · crear contenedor. 

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/docker/IMG/36.png)

  · Comprobar el acceso a "holamundo3.html".

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/docker/IMG/37.png)

# 5. Docker Hub #

## 5.1 Creamos los ficheros necesarios ##

  · Crear carpeta dockerXXpush. Entrar en la carpeta.
  · Crear un script (holamundoXX.sh) con lo siguiente:

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/docker/IMG/38.png)

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/docker/IMG/39.png)

  · Crear fichero Dockerfile.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/docker/IMG/40.png)

  · A partir del Dockerfile anterior crearemos la imagen.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/docker/IMG/41.png)

  · Comprobar que docker run nombre-alumno/holamundo se crea un contenedor que ejecuta el script.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/docker/IMG/42.png)

## 5.2 Subir la imagen a Docker Hub ##

  · Registrarse en Docker Hub.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/docker/IMG/43.png)

  · docker login -u USUARIO-DOCKER, para abrir la conexión.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/docker/IMG/44.png)

    · Este punto me daba error y no pude solucionarlo.

# 6. Limpiar contenedores e imágenes #

  · docker ps -a, identificar todos los contenedores que tenemos.

  · docker rm ..., eliminar los contenedores.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/docker/IMG/45.png)

  · docker images, identificar todas las imágenes.

  · docker rmi ..., eliminar las imágenes.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/docker/IMG/46.png)

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/docker/IMG/47.png)

