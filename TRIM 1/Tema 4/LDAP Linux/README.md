# LDAP Linux - Christian Moreno #

## 2. Instalar el Servidor LDAP

## 2.1 Instalación del paquete
  
  - Instalamos el paquete.
 
![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%204/LDAP%20Linux/IMG/1.png)

  - Comprobar que la versión es >= 1.4.*

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%204/LDAP%20Linux/IMG/2.png)

## 2.2 Configurar la instancia

  - Crear el fichero /root/instance.inf con el siguiente contenido. 

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%204/LDAP%20Linux/IMG/3.png)

  - Creamos una nueva instancia.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%204/LDAP%20Linux/IMG/4.png)

  - Comprobar el estado actual de la instancia de la base de datos LDAP.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%204/LDAP%20Linux/IMG/5.png)

  - Creamos el fichero /root/.dsrc con el siguiente contenido.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%204/LDAP%20Linux/IMG/6.png)

## 2.3 Abrir los puertos del cortafuegos

  - Podemos abrir los puertos "ldap" y "ldaps" por el cortafuegos de Yast.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%204/LDAP%20Linux/IMG/7.png)

## 2.4 Comprobamos el servicio

  - Comprobar que el servidor LDAP es accesible desde la red.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%204/LDAP%20Linux/IMG/8.png)

## 2.5 Comprobamos el acceso al contenido del LDAP

  - El primer comando muestra el contenido de nuestra base de datos LDAP.
  - El segundo comando hace la consulta usando usuario/clave.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%204/LDAP%20Linux/IMG/9.png)

## 3. Usuarios LDAP

## 3.1 Buscar Unidades Organizativas

  - Ejecutamos el comando para buscar la OU:

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%204/LDAP%20Linux/IMG/10.png)

## 3.2 Agregar usuarios

  - Fichero mazinger-add.ldif con la información para crear el usuario mazinger.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%204/LDAP%20Linux/IMG/11.png)

  - Escribir los datos del fichero ldif anterior dentro de LDAP.
  
![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%204/LDAP%20Linux/IMG/12.png)

## 3.3 Comprobar el nuevo usuario

  - Comprobar si se ha creado el usuario correctamente en el LDAP.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%204/LDAP%20Linux/IMG/13.png)

## 4. Agregar más usuarios

## 4.1 Agregar los siguientes usuarios

  - Creamos una contraseña encriptada, yo utilicé slappasswd.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%204/LDAP%20Linux/IMG/14.png)

  - Creamos usuario koji kabuto.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%204/LDAP%20Linux/IMG/15.png)

  - Creamos usuario Boss.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%204/LDAP%20Linux/IMG/16.png)

  - Creamos usuario Doctor Infierno.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%204/LDAP%20Linux/IMG/17.png)

  - Añadimos a los usuarios.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%204/LDAP%20Linux/IMG/18.png)

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%204/LDAP%20Linux/IMG/19.png)

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%204/LDAP%20Linux/IMG/20.png)

## 4.2 Comprobar desde el cliente

  - Comprobar que el puerto LDAP del servidor está abierto.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%204/LDAP%20Linux/IMG/21.png)

  - Consultar los usuarios LDAP que tenemos en el servicio de directorio remoto.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%204/LDAP%20Linux/IMG/22.png)

# NOTA

  - No encontré explicación a el porqué no salen los demás usuarios que cree y añadí.
