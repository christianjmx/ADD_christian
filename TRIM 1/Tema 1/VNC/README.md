# Acceso remoto VNC #
## Christian José Moreno Expósito ##

# VNC Windows #

## Máquina Slave ##

· Descargamos el tightVNC.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%201/VNC/IMG/VNC%20Windows/1.png)

· Instalamos el tightVNC .

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%201/VNC/IMG/VNC%20Windows/1.1.png)

(configuramos las contraseñas de acceso)

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%201/VNC/IMG/VNC%20Windows/1.2.png)


### 1.2 Comprobamos desde una máquina GNU/Linuz que los servicios son visibles desde fuera ###

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%201/VNC/IMG/VNC%20Windows/1.3.png)

### 2 Instalamos el windows viewer en la Máquina Master ###

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%201/VNC/IMG/VNC%20Windows/1.4.png)


  · Configuramos el TightVNC server.
  
![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%201/VNC/IMG/VNC%20Windows/1.5.png)


  · Habilitamos la regla TightVNC en el firewall de la máquina SLAVE.
  
 ![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%201/VNC/IMG/VNC%20Windows/1.7.png)
 
  · En la máquina Master entramos en el TightVNC Viewer y escribimos la ip del Slave y el puerto.
  
 ![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%201/VNC/IMG/VNC%20Windows/1.8.png)
 
  · Escribimos la contraseña.
  
 ![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%201/VNC/IMG/VNC%20Windows/1.9.png)
 
  · Ya estaríamos conectador por VNC.
  
 ![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%201/VNC/IMG/VNC%20Windows/2.0.png)
 
 
 
 # VNC Linux #
 ## Desde la máquina Slave Opensuse ##
 
 · Configuramos una dirección estática (En mi caso tuve que dejarlas en dinamicas ya que realicé la tarea desde mi casa)
 
 ![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%201/VNC/IMG/VNC%20Opensuse/1.1.png)
 
 · Configuramos VNC desde yast.
 
 ![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%201/VNC/IMG/VNC%20Opensuse/1.2.png)
 
 · Permitimos la administración remota.
 
 ![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%201/VNC/IMG/VNC%20Opensuse/1.3.png)
 
 · Ejecutamos VNCServer por comando.
 
 ![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%201/VNC/IMG/VNC%20Opensuse/1.4.png)
 
 · Comprobamos los servicios en ejecución.
 
 ![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%201/VNC/IMG/VNC%20Opensuse/1.5.png)

  · Comprobamos que están los servicios en los puertos correctos.
  
 ![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%201/VNC/IMG/VNC%20Opensuse/1.6.png)


### Desde una máquina GNU/Linux ###

  · Comprobamos si son visibles los servicios desde fuera.
  
 ![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%201/VNC/IMG/VNC%20Opensuse/1.7.png)
 
## Desde la máquina Master Opensuse ##

  · Nos conectamos por comando a la maquina Slave poniendo la IP y contraseña.
  
 ![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%201/VNC/IMG/VNC%20Opensuse/1.8.png)
 
  · Conexión correcta
 
 ![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%201/VNC/IMG/VNC%20Opensuse/1.9.png)
 
 ## Comprobaciones finales ##
 
  · Desde La máquina master ejecutamos el siguiente comando para ver las conexiones.
  
 ![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%201/VNC/IMG/VNC%20Opensuse/2.0.png)
 
  · Ejecutamos el siguiente comando en el servidor.
  
 ![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%201/VNC/IMG/VNC%20Opensuse/2.1.png)


# SSOO Cruzados #

· Conectar el cliente GNU/Linux con el Servidor VNC Windows.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%201/VNC/IMG/VNC%20Opensuse/4.1.png)

· Comprobaación de conexión.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%201/VNC/IMG/VNC%20Opensuse/4.2.png)

· Comprobación de direcciones remotas desde windows.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%201/VNC/IMG/VNC%20Opensuse/4.3.png)


# 6. DISPLAY 0 en GNU/Linux #

  · Ir al servidor y ejecutar el siguiente comando.
  
 ![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%201/VNC/IMG/VNC%20Opensuse/5.1.png)
 
  · Desde el cliente comprobar los puertos del servidor.
 
 ![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%201/VNC/IMG/VNC%20Opensuse/5.2.png)
 
  · Conectarnos con el servidor.
  
 ![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%201/VNC/IMG/VNC%20Opensuse/5.3.png)
 
  · Conectado correctamente.
  
 ![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%201/VNC/IMG/VNC%20Opensuse/5.4.png)
 
  · Comprobación de conexión.
  
 ![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%201/VNC/IMG/VNC%20Opensuse/5.5.png)






