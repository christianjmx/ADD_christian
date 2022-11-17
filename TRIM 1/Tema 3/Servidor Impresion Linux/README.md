# Servidor de impresión Linux - Christian Moreno #

## 2. Servidor de Impresión ##

- Comprobamos que el servicio está en ejecución.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%203/Servidor%20Impresion%20Linux/IMG/1.png)

- Modificamos el fichero cupsd.conf de la siguiente manera.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%203/Servidor%20Impresion%20Linux/IMG/2.png)

- Reiniciamos el servicio y comprobamos el estado.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%203/Servidor%20Impresion%20Linux/IMG/3.png)

- En la configuración del firewall añadimos ipp y ipp-client al corta fuegos.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%203/Servidor%20Impresion%20Linux/IMG/4.png)

- Ahora conectamos con la interfaz web de CUPS.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%203/Servidor%20Impresion%20Linux/IMG/5.png)

- Ahora vamos a ver el archivo de registro de accesos desde el apartado administración, con el usuario root.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%203/Servidor%20Impresion%20Linux/IMG/6.png)

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%203/Servidor%20Impresion%20Linux/IMG/7.png)

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%203/Servidor%20Impresion%20Linux/IMG/8.png)


## 3. Imprimir de forma local ##

- Instalamos el paquete cups-pdf desde consola.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%203/Servidor%20Impresion%20Linux/IMG/10.png)

- Añadimos una nueva impresora desde el apartado de administración.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%203/Servidor%20Impresion%20Linux/IMG/9.png)

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%203/Servidor%20Impresion%20Linux/IMG/11.png)

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%203/Servidor%20Impresion%20Linux/IMG/12.png)

- Creamos el archivo que vamos a imprimir.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%203/Servidor%20Impresion%20Linux/IMG/13.png)

- Procedemos a imprimirlo y comprobamos que se ha impreso.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%203/Servidor%20Impresion%20Linux/IMG/14.png)

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%203/Servidor%20Impresion%20Linux/IMG/15.png)

- Esto es lo más entendible al visualizar el pdf.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%203/Servidor%20Impresion%20Linux/IMG/16.png)

## 4. Imprimir de forma remota ##

- En la web modificamos la impresora para habilitar como recurso compartido.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%203/Servidor%20Impresion%20Linux/IMG/17.png)

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%203/Servidor%20Impresion%20Linux/IMG/18.png)

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%203/Servidor%20Impresion%20Linux/IMG/19.png)

- Ahora en el cliente añadimos el ipp y ipp-client en el firewall.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%203/Servidor%20Impresion%20Linux/IMG/20.png)

- Compruebo que puedo acceder a la página de cups desde el cliente.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%203/Servidor%20Impresion%20Linux/IMG/21.png)

- Ahora desde la herramienta configuración de impresión, añadimos la impresora de red.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%203/Servidor%20Impresion%20Linux/IMG/22.png)

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%203/Servidor%20Impresion%20Linux/IMG/23.png)

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%203/Servidor%20Impresion%20Linux/IMG/24.png)

- Creamos el archivo que vamos a imprimir desde el cliente.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%203/Servidor%20Impresion%20Linux/IMG/25.png)

- Procedemos a imprimir y comprobar desde el servidor si se imprimió remotamente.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%203/Servidor%20Impresion%20Linux/IMG/26.png)

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%203/Servidor%20Impresion%20Linux/IMG/27.png)

- Esto es el contenido mas legible al visualizarlo.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%201/Tema%203/Servidor%20Impresion%20Linux/IMG/28.png)
