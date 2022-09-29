# Clientes Ligeros #
## Christian Moreno ##

### Preparación de MV Server ###

 · Configuramos dos interfaces de RED, Una Externa para tener acceso a internet con adaptador puente y otra interna con la IP que se especifica.
 ![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%201/Clientes%20ligeros/Capturas%20ADD%20clientes%20lgeros/3.1.png)
 
 ![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%201/Clientes%20ligeros/Capturas%20ADD%20clientes%20lgeros/3.2.png)
 
 
 · Configuramos las IP estaticas de las interfaces de RED en la MV.
 
 (Externa)
 ![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%201/Clientes%20ligeros/Capturas%20ADD%20clientes%20lgeros/3.3.png)
 
 (Interna)
 ![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%201/Clientes%20ligeros/Capturas%20ADD%20clientes%20lgeros/3.4.png)
 
 ### Instalación del SSOO ###
 
 · Ejecutamos los siguientes comando:
 
 (IP a)
 ![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%201/Clientes%20ligeros/Capturas%20ADD%20clientes%20lgeros/3.5.png)
 
 (Hostname -n, hostname -f, uname -a, sudo blkid)
 ![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%201/Clientes%20ligeros/Capturas%20ADD%20clientes%20lgeros/3.6.png)
 
 
 · Creamos dos usuarios con contraseña Con nuestro apellido.
 ![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%201/Clientes%20ligeros/Capturas%20ADD%20clientes%20lgeros/3.7.png)
 
 ### Instalar el servicio LTSP ###
 
 · Escribimos los siguientes comandos para la instalación de LTSP:
 
 ![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%201/Clientes%20ligeros/Capturas%20ADD%20clientes%20lgeros/3.8.png)
 
 (añadimos nuestro usuario al grupo epoptes)
 (configuramos dnsmasq)
 ![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%201/Clientes%20ligeros/Capturas%20ADD%20clientes%20lgeros/3.9.png)
 
 
 · Creamos una imagen SO de los clientes ligeros.
 
 ![images](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%201/Clientes%20ligeros/Capturas%20ADD%20clientes%20lgeros/4.0.png)
 
 · Consultamos la información.
 
 ![images](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%201/Clientes%20ligeros/Capturas%20ADD%20clientes%20lgeros/4.1.png)
 
 ### Configuración ###
 
 · Generamos el menú iPXE (ltsp ipxe)
 · Configurar el servidor LTSP para servir imágenes NFS (ltsp nfs)
 · Generar ltsp.img (ltsp initrd)
 
 ![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%201/Clientes%20ligeros/Capturas%20ADD%20clientes%20lgeros/4.2.png)
 
 ### Preparar la MV Cliente ###
 
 · Creamos una MV sin disco duro y sin unidad DVD.
 
 ![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%201/Clientes%20ligeros/Capturas%20ADD%20clientes%20lgeros/4.3.png)
 
 · Tarjeta de RED en modo Interna.
 
 ![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%201/Clientes%20ligeros/Capturas%20ADD%20clientes%20lgeros/4.4.png)
 
 · Seleccionamos el modo de arranque en tipo RED.
 
 ![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%201/Clientes%20ligeros/Capturas%20ADD%20clientes%20lgeros/4.5.png)
 
 · Configuramos la memoria gráfica a 128MB y habilitamos el soporte 3D.
 
 ![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%201/Clientes%20ligeros/Capturas%20ADD%20clientes%20lgeros/4.6.png)
 
 · Iniciamos la máquina Cliente con la máquina servidor encendida.
 
 Seleccionamos la imagen que creamos en la RED.
 ![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%201/Clientes%20ligeros/Capturas%20ADD%20clientes%20lgeros/4.7.png)
 
 · Ahora Se nos debería iniciar el SO ligero y podernos conectar con nuestros usuarios. En mi caso no pude hacerlo ya que por dos veces consecutivas dio un error de red y no cargaba el SO ligero.
 
![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%201/Clientes%20ligeros/Capturas%20ADD%20clientes%20lgeros/4.9.png)
 

 
