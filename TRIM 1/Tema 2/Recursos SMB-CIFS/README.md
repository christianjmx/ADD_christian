# Samba (OpenSUSE y Windows) - Christian Moreno #

## 1.1 Preparativos ##

- Cambiamos el nombre del equipo y añadimos los nombres de los equipos cliente.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%202/Recursos%20SMB-CIFS/IMG/Samba/1.png)

## 1.2 Usuarios Locales ##

- Creamos los grupos indicados (piratas,soldados,sambausers)

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%202/Recursos%20SMB-CIFS/IMG/Samba/2.png)

- Cremos los usuarios que nos pide, dentro de sus respectivos grupos.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%202/Recursos%20SMB-CIFS/IMG/Samba/3.png)

- El usuario sambaguest le cambiamos el tipo de shell.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%202/Recursos%20SMB-CIFS/IMG/Samba/4.png)

## 1.3  Crear las carpetas para los futuros recursos compartidos ##

- Creamos la carpeta base para los recursos y le damos los permisos.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%202/Recursos%20SMB-CIFS/IMG/Samba/5.png)

- Creamos las carpetas de los recursos compartidos.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%202/Recursos%20SMB-CIFS/IMG/Samba/6.png)

(visualizamos si se cambiaron el grupo y el usuario propietario)

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%202/Recursos%20SMB-CIFS/IMG/Samba/7.png)

- Repetimos lo mismo con los otros dos recursos.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%202/Recursos%20SMB-CIFS/IMG/Samba/8.png)

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%202/Recursos%20SMB-CIFS/IMG/Samba/9.png)

## 1.4 Configurar el servidor Samba ##

- Hacemos una copia de seguridad del fichero.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%202/Recursos%20SMB-CIFS/IMG/Samba/10.png)

- Vamos al yast ---> Samba Server

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%202/Recursos%20SMB-CIFS/IMG/Samba/11.png)

 (Configuramos que al reiniciar se active)
![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%202/Recursos%20SMB-CIFS/IMG/Samba/12.png)

## 1.5 Crear los recursos compartidos de red ##

- Modificamos el fichero de configuración smb.conf

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%202/Recursos%20SMB-CIFS/IMG/Samba/13.png)

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%202/Recursos%20SMB-CIFS/IMG/Samba/14.png)

- Comprobamos que la sintaxis está correcta.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%202/Recursos%20SMB-CIFS/IMG/Samba/15.png)

## 1.6 Usuarios Samba ##

- Creamos las claves para los Usuarios samba (repetimos este proceso con todos los usuarios).

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%202/Recursos%20SMB-CIFS/IMG/Samba/16.png)

- Comprobamos la lista de Usuarios Samba

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%202/Recursos%20SMB-CIFS/IMG/Samba/17.png)

## 1.7 Reiniciar ##

- Reiniciamos el servicio smb y nmb y comprobamos que el servicio esté ecuchando.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%202/Recursos%20SMB-CIFS/IMG/Samba/18.png)

## 2 Windows ##

- Configuramos el fichero hosts del cliente windows.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%202/Recursos%20SMB-CIFS/IMG/Samba/19.png)

## 2.1 Cliente Windows GUI ##

- Accedemos a los recursos compartidos del servidor samba.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%202/Recursos%20SMB-CIFS/IMG/Samba/20.png)

- Accedemos al recurso public09.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%202/Recursos%20SMB-CIFS/IMG/Samba/21.png)

- Accedemos al recurso compartido castillo09 con usuario soldado1.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%202/Recursos%20SMB-CIFS/IMG/Samba/22.png)

- Vemos las conexiones abiertas.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%202/Recursos%20SMB-CIFS/IMG/Samba/23.png)

- Borramos las conexiones SMB/CIFS

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%202/Recursos%20SMB-CIFS/IMG/Samba/24.png)

- Acceder al recurso compartido barco09 con usuario pirata1.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%202/Recursos%20SMB-CIFS/IMG/Samba/25.png)

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%202/Recursos%20SMB-CIFS/IMG/Samba/26.png)

- En el servidor samba observamos los resultados de los comandos que se indican:

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%202/Recursos%20SMB-CIFS/IMG/Samba/27.png)

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%202/Recursos%20SMB-CIFS/IMG/Samba/28.png)

## 2.2 Cliente Windows comandos ##

- Vemos los recursos del servidor remoto.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%202/Recursos%20SMB-CIFS/IMG/Samba/29.png)

- Montar el recurso barco09 de forma persistente.
- crear una conexión y lo monta en la unidad S

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%202/Recursos%20SMB-CIFS/IMG/Samba/30.png)

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%202/Recursos%20SMB-CIFS/IMG/Samba/31.png)

- Comprobamos con net use.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%202/Recursos%20SMB-CIFS/IMG/Samba/32.png)

- Ahora podemos crear carpetas desde la unidad S:

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%202/Recursos%20SMB-CIFS/IMG/Samba/33.png)

- En el servidor samba observamos los resultados de los comandos que se indican:

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%202/Recursos%20SMB-CIFS/IMG/Samba/34.png)

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%202/Recursos%20SMB-CIFS/IMG/Samba/35.png)

## 3 Cliente GNU/Linux ##

- Configuramos el archivo /etc/hosts

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%202/Recursos%20SMB-CIFS/IMG/Samba/36.png)

- Nos conectamos a los recursos compartidos graficamente.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%202/Recursos%20SMB-CIFS/IMG/parte%20de%20grafico/80.png)

- Nos conectamos a catillo09 y barco09 y creamos carpetas en ellos.
(castillo09)
![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%202/Recursos%20SMB-CIFS/IMG/parte%20de%20grafico/81.png)

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%202/Recursos%20SMB-CIFS/IMG/parte%20de%20grafico/82.png)

(barco09)
![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%202/Recursos%20SMB-CIFS/IMG/parte%20de%20grafico/83.png)

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%202/Recursos%20SMB-CIFS/IMG/parte%20de%20grafico/84.png)

- En el servidor samba observamos los resultados de los comandos que se indican:

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%202/Recursos%20SMB-CIFS/IMG/parte%20de%20grafico/85.png)

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%202/Recursos%20SMB-CIFS/IMG/parte%20de%20grafico/86.png)






























