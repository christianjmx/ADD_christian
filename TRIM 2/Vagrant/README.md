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

### 3.3 Comprobamos ###

· vagrant up, para crear la MV.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/Vagrant/IMG/25.png)

· Para verificar que efectivamente el servidor Apache ha sido instalado e iniciado, abrimos navegador en la máquina real con URL http://127.0.0.1:42XX.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/Vagrant/IMG/26.png)

## 4. Proyecto: Suministro mediante Puppet ##

### 4.1 Preparativos ###

· Crear directorio nombre-alumnoXX-va4puppet.d como nuevo proyecto Vagrant.
· Modificar el archivo Vagrantfile de la siguiente forma:

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/Vagrant/IMG/27.png)

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/Vagrant/IMG/28.png)

· Crear la carpeta manifests. 
· Crear el fichero manifests/nombre-del-alumnoXX.pp, con las órdenes/instrucciones Puppet necesarias para instalar el software que elijamos. Ejemplo:

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/Vagrant/IMG/29.png)

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/Vagrant/IMG/30.png)


"Punto 4.2 ya etá hecho"


### 4.3 Comprobamos ###

· Ir a la MV:
  · Comprobar que el software está instalado.
  
![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/Vagrant/IMG/31.png)

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/Vagrant/IMG/32.png)

## 5. Proyecto: Caja personalizada ##

### 5.1 Preparar la MV VirtualBox ###

· Ir a la MV de VirtualBox.
· Poner clave "vagrant" al usuario root.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/Vagrant/IMG/34.png)

· Configuramos acceso por clave pública al usuario vagrant:
  · mkdir -pm 700 /home/vagrant/.ssh, creamos la carpeta de configuración SSH.
  · wget --no-check-certificate 'https://raw.github.com/mitchellh/vagrant/master/keys/vagrant.pub' -O /home/vagrant/.ssh/authorized_keys, descargamos la clave pública.
  · chmod 0600 /home/vagrant/.ssh/authorized_keys, modificamos los permisos de la carpeta.
  · chown -R vagrant /home/vagrant/.ssh, modificamos el propietario de la carpeta.
  
![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/Vagrant/IMG/35.png)

### Sudoers ###

· Añadir vagrant ALL=(ALL) NOPASSWD: ALL al fichero de configuración /etc/sudoers

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/Vagrant/IMG/36.png)

### 5.2 Crear caja Vagrant ###

· Vamos a crear una nueva carpeta nombre-alumnoXX-va5custom.d
· VBoxManage list vms, comando de VirtualBox que muestra los nombres de nuestras MVs. 

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/Vagrant/IMG/37.png)

· vagrant package --base VMNAME --output nombre-alumnoXX.box, parar crear nuestra propia caja.
· Comprobamos que se ha creado el fichero nombre-alumnoXX.box
· vagrant box add nombre-alumno/va5custom nombre-alumnoXX.box, añadimos la nueva caja creada por nosotros, al repositorio local de cajas vagrant de nuestra máquina.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/Vagrant/IMG/38.png)

· Consultar ahora la lista de cajas Vagrant disponibles.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/Vagrant/IMG/39.png)

### 5.3 Vagrantfile ###

· Crear un nuevo fichero Vagrantfile para usar nuestra caja.
· Incluir en el fichero Vagrantfile las configuraciones necesarias para:
  · La MV de VirtualBox debe tener el nombre vagrantXX-nombre-alumno.
  · La memoria RAM de la MV en VirtualBox debe ser de 2048 MiB.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/Vagrant/IMG/40.png)

### 5.4 Usar la nueva caja ###

· Levantamos una nueva MV a partir del Vagranfile.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/Vagrant/IMG/41.png)

· Nos debemos conectar sin problemas (vagant ssh).

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/Vagrant/IMG/42.png)

## 6. Caja Windows ##

### 6.1 Windows con vagrant ###

· Crear una MV Windows usando vagrant.
· Comprobar que funciona.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/Vagrant/IMG/43.png)

· Archivo vagrantfile

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/Vagrant/IMG/44.png)

· Instalamos el plugin winrm

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/Vagrant/IMG/46.png)

· Levantamos la máquina.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/Vagrant/IMG/45.png)

