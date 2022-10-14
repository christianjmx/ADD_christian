# Acceso Remoto SSH - Christian Moreno #

## 1.1 Servidor SSH ##

- Creamos los 4 usuarios que se pidden.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%201/SSH/capturas/1.1/1.png)

- Realizamos la comprobación de los comandos que se piden. (Yo tuve que dejar las IPs dinamicas en todos las
MV ya que los hice desde mi casa y no conseguí ponerlas estáticas y qie funcionara todo bien)

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%201/SSH/capturas/1.1/2.png)

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%201/SSH/capturas/1.1/3.png)

## 1.2 Cliente GNU/Linux ##

- Añadimos los equipos server09g y cliente09w al fichero hosts del cliente.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%201/SSH/capturas/1.2/1.png)

- Comprobamos que hace ping a los dos equipos.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%201/SSH/capturas/1.2/2.png)

## 1.3 Cliente Windows ##

- Descargamos e instalamos el software PuTTY

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%201/SSH/capturas/1.3/1.png)

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%201/SSH/capturas/1.3/2.png)

- Añadimos en el fichero hosts del cliente windows los equipos server09g y cliente09g.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%201/SSH/capturas/1.3/3.png)

- Comprobamos que hace ping a los dos equipos.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%201/SSH/capturas/1.3/4.png)

## 2.1 Comprobación ##

- Comprobamos que el OpenSSH esté instalado 

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%201/SSH/capturas/2.1/1.png)

- Comprobamos que el servicio está escuchando por el puerto 22.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%201/SSH/capturas/2.1/2.png)

## 2.2 Primera Conexión SSH desde cliente GNU/Linux ##

- Comprobamos la conectividad con el servidor con ping y comprobamos que el puerto 22 esté abierto.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%201/SSH/capturas/2.2/1.png)

- Comprobamos que conecta por SSH al servidor.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%201/SSH/capturas/2.2/2.png)

- Observamos el contenido del fichero especificado.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%201/SSH/capturas/2.2/3.png)

## 2.3 Primera conexión SSH desde cliente Windows ##















