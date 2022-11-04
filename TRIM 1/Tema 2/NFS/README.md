# NFS - Christian Moreno #

- Instalamos el servicio NFS.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%202/NFS/IMG/1.png)

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%202/NFS/IMG/2.png)

- Creamos la carpeta public y la compartimos con NFS dandole los permisos adecuados.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%202/NFS/IMG/3.png)

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%202/NFS/IMG/4.png)

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%202/NFS/IMG/5.png)

- Ahora creamos la private y hacemos lo mismo, pero con distintos permisos.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%202/NFS/IMG/6.png)

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%202/NFS/IMG/7.png)

- Comprobamos los recursos exportados.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%202/NFS/IMG/8.png)

- Instalamos el soporte en el cliente, desde los archivos de programa.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%202/NFS/IMG/9.png)

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%202/NFS/IMG/10.png)

- Verificamos que el servicio se inicio en el cliente.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%202/NFS/IMG/11.png)

- Montamos el recurso.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%202/NFS/IMG/12.png)

- Verificamos el montaje.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%202/NFS/IMG/13.png)

- Creamos una carpeta desde el cliente para confirmar que se crea.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%202/NFS/IMG/14.png)

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%202/NFS/IMG/15.png)

## NFS - Linux ##

-Instalamos desde yast el servicio servidor  nfs.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%202/NFS/IMG/16.png)

- CReamos las carpetas correspondiente y les ponemos grupo, usuario y permisos.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%202/NFS/IMG/17.png)

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%202/NFS/IMG/18.png)

- Añadimos las líneas correspondientes al fichero /etc/exports.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%202/NFS/IMG/19.png)

- Revisamos si hay conexión con el servidor.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%202/NFS/IMG/20.png)

- En este paso no logé que montara nada utilizando el servidor de linux. no conseguí arreglarlo. daba el siguiente fallo:

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%202/NFS/IMG/21.png)

 # Preguntas #
 
 - ¿Nuestro cliente GNU/Linux NFS puede acceder al servidor Windows NFS?

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%202/NFS/IMG/22.png)

- ¿Nuestro cliente Windows NFS podría acceder al servidor GNU/Linux NFS?

Al igual que la anterior, si es posible conectar.

- Fijarse en los valores de usuarios propietario y grupo propietario de los
ficheros que se guardan en el servidor NFS, cuando los creamos desde una
conexión cliente NFS.

obtiene los valores establecidos en el servidor.

























