# Acceso Remoto SSH - Christian Moreno #

## 1.1 Servidor SSH ##

- Creamos los 4 usuarios que se piden.

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

- Desde el cliente Windows (usando PuTTY) nos conectamos al servidor SSH de GNU/Linux.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%201/SSH/capturas/2.3/1.png)

- Observamos la clave.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%201/SSH/capturas/2.3/2.png)

- Confimamos la conexión.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%201/SSH/capturas/2.3/3.png)

## 3. Cambiamos la identidad del servidor ##

- Confirmar que existen los ficheros ssh_host*key y ssh_host*key.pub.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%201/SSH/capturas/3/1.png)

- Descomentamos la línea que se indica.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%201/SSH/capturas/3/2.png)

## 3.1 Regenerar certificados ## 

- Generamos una nueva clave publica/privada:

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%201/SSH/capturas/3.1/1.png)

- Reiniciamos el servicio y comprobamos que el estado sea correcto.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%201/SSH/capturas/3.1/2.png)

## 3.2 Comprobamos ##

- Intentamos conectar con el usuario moreno1 dede linux y da error.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%201/SSH/capturas/3.2/1.png)

- Intentamos conectar con el usuario moreno2 dede linux y da error.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%201/SSH/capturas/3.2/2.png)

- Intentamos conectar con el usuario moreno1 dede windows y no da error.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%201/SSH/capturas/3.2/3.png)

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%201/SSH/capturas/3.2/4.png)

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%201/SSH/capturas/3.2/5.png)

- En linux escribimos el siguiente comando para solucionar el problema.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%201/SSH/capturas/3.2/6.png)

- Comprobamos otra vez la conexión con los dos usuarios desde el cliente linux.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%201/SSH/capturas/3.2/7.png)

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%201/SSH/capturas/3.2/8.png)

## 4. Personalización del prompt Bash ##

- Modificamos el fichero Fichero /home/moreno1/.bashrc)

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%201/SSH/capturas/4/1.png)

- Creamos los siguientes alias:

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%201/SSH/capturas/4/2.png)

- Comprobamos que funciona la concexión ssh con cada cliente

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%201/SSH/capturas/4/3.png)

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%201/SSH/capturas/4/4.png)

## 5. Autenticación mediante claves públicas ##

- Generamos un nuevo par de claves para el usuario.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%201/SSH/capturas/5/1.png)

- Copiamos la clave publica al fichero especificado que está en el servidor.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%201/SSH/capturas/5/2.png)

- Comprobamos que con el usuario moreno4 no hace falta escribir una contraseña desde el cliente linux.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%201/SSH/capturas/5/4.png)

- Al contrario que antes... comprobamos que desde el cliente windows si hace falta escribir una contraseña para conectarse.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%201/SSH/capturas/5/5.png)

## 6. Uso de SSH como túnel para X ##

- Instalamos el geany en el servidor (ya que no está instalado en el cliente)

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%201/SSH/capturas/6/1.png)

- Vamos al fichero de configuración del ssh y desmarcamos esta línea:

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%201/SSH/capturas/6/2.png)

- Comprobamos en el cliente que no está instalado el geany.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%201/SSH/capturas/6/3.png)

- Iniciamos sesión mediante ssh con el servidor y ejecutamos geany.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%201/SSH/capturas/6/4.png)

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%201/SSH/capturas/6/5.png)

## 7. Aplicaciones Windows nativas ##

- Instalamos wine en el servidor linux.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%201/SSH/capturas/7/1.png)

- nos conectamos por ssh al servidor y ejecutamos wine con una aplicación de windows en este caso notepad.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%201/SSH/capturas/7/2.png)

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%201/SSH/capturas/7/3.png)


## Los puntos 8 y 9 no los pude hacer ya que la práctica la quería retomar hoy domingo y no me funcionaron las máquinas en mi casa, y no me da tiempo de 
entregarlo a tiempo. ##













