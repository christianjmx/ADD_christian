# Vagrant - Christian Moreno #

## 1. Proyecto: Añadir cajas ##

### 1.1 Imagen, caja o box ###

· Comprobar la versión actual de Vagrant.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/Vagrant/IMG/1.png)

· Descargar la caja que necesitamos a través de vagrant.
· Lista las cajas/imágenes disponibles actualmente en nuestra máquina.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/Vagrant/IMG/2.png)

### 1.2 Directorio ###

· Crear un directorio para nuestro proyecto.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/Vagrant/IMG/3.png)

· Crear un fichero nuevo llamado Vagrantfile con el siguiente contenido:

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/Vagrant/IMG/4.png)

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/Vagrant/IMG/5.png)

### 1.3 Comprobar ###

· Iniciar una nueva instancia de la máquina.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/Vagrant/IMG/6.png)

· Conectar/entrar en nuestra máquina virtual usando SSH.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/Vagrant/IMG/7.png)

### 1.4 Eliminamos la MV ###

· exit para Salir fuera de la MV.
· vagrant halt, para apagar la máquina virtual.
· vagrant status, consultar el estado actual de la máquina virtual.
· vagrant destroy, para eliminar la máquina virtual.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/Vagrant/IMG/8.png)

## 2. Proyecto: Redirección de puertos ##

### 2.1 Creamos los ficheros ###

· Crear carpeta nombre-alumnoXX-va2port.d.
· Configurar Vagrantfile para usar nuestra caja BOXNAME y hostname = "nombre-alumnoXX-vagrant3".
· Modificar el fichero Vagrantfile, de modo que el puerto 42XX del sistema anfitrión sea enrutado al puerto 80 del ambiente virtualizado.

· Incluir en el fichero Vagrantfile las configuraciones necesarias para:
  · La MV de VirtualBox debe tener el nombre vagrantXX-va2port.
  · La memoria RAM de la MV en VirtualBox debe ser de 2048 MiB.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/Vagrant/IMG/9.png)

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/Vagrant/IMG/10.png)

· Levantar la MV podemos hace vagrant up pero también time vagrant up para medir el tiempo que se tarda en levantar la MV.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/Vagrant/IMG/11.png)

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/Vagrant/IMG/12.png)

### 2.2 Entramos en la MV ###

· Entramos en la MV en la máquina virtual
· Instalamos Apache2.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/Vagrant/IMG/13.png)

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/Vagrant/IMG/14.png)

### 2.3 Comprobar ###

· Ir a la máquina real.
· vagrant port para ver la redirección de puertos de la máquina Vagrant.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/Vagrant/IMG/15.png)

· Abrir el navegador web con el URL http://127.0.0.1:42XX. En realidad estamos accediendo al puerto 80 de nuestro sistema virtualizado.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/Vagrant/IMG/16.png)

· nmap -Pn localhost

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/Vagrant/IMG/17.png)

### 2.4 Eliminar la MV ###

· Eliminamos la MV

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/Vagrant/IMG/18.png)

## 3. Proyecto: Suministro mediante shell script ##

### 3.1 Crear ficheros ###

· Crear directorio nombre-alumnoXX-va3script.d para nuestro proyecto.
· Crear la carpeta html y crear fichero html/index.html con el siguiente contenido:

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/Vagrant/IMG/19.png)

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/Vagrant/IMG/20.png)

· Crear el script install_apache.sh, dentro del proyecto con el siguiente contenido:

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/Vagrant/IMG/21.png)

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/Vagrant/IMG/22.png)

### 3.2 Vagrantfile ###

· Incluir en el fichero de configuración Vagrantfile lo siguiente:
  · config.vm.hostname = "nombre-alumnoXX-va3script"
  · config.vm.provision :shell, :path => "install_apache.sh"
  · config.vm.synced_folder "html", "/var/www/html"
  https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/Vagrant/IMG/24.png
· Incluir en el fichero Vagrantfile las configuraciones necesarias para:
  · La MV de VirtualBox debe tener el nombre vagrantXX-va3script.
  · La memoria RAM de la MV en VirtualBox debe ser de 2048 MiB.
  
![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/Vagrant/IMG/23.png)

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/Vagrant/IMG/24.png)






























