# Salt-stack  -  Christian Moreno #

## 2. Master: Instalar y configurar ##

instalar el software del Máster.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/salt-stack/IMG/1.png)

Modificar /etc/salt/master para configurar nuestro Máster con:

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/salt-stack/IMG/2.png)

systemctl enable salt-master.service, activiar servicio en el arranque del sistema.

systemctl start salt-master.service, iniciar servicio.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/salt-stack/IMG/3.png)

salt-key -L, para consultar Minions aceptados por nuestro Máster. Vemos que no hay ninguno todavía.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/salt-stack/IMG/4.png)

## 3. Minion ##

### 3.1 Instalación y configuración ###

zypper install salt-minion, instalar el software del agente (minion).

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/salt-stack/IMG/5.png)

Modificar /etc/salt/minion para definir quien será nuestro Máster:

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/salt-stack/IMG/6.png)

systemctl enable salt-minion.service, activar Minion en el arranque del sistema.

systemctl start salt-minion.service, iniciar el servico del Minion.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/salt-stack/IMG/7.png)

### 3.3 Aceptación desde el Master ###

Ir a MV1:

salt-key -L, vemos que el Máster recibe petición del Minion.

salt-key -a minionXXg, para que el Máster acepte a dicho Minion.

salt-key -L, comprobamos.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/salt-stack/IMG/8.png)

### 3.4 Comprobamos conectividad ###

Conectividad hacia los Minions.

Versión de Salt instalada en los Minions

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/salt-stack/IMG/9.png)

## 4. Salt States ##

### 4.1 Preparar el directorio para los estados ###

Ir a la MV Máster:

Crear el directorio /srv/salt/base(para guardar nuestros estados), y el directorio /srv/salt/devel (para desarrollo o para hacer pruebas).

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/salt-stack/IMG/10.png)

Crear archivo /etc/salt/master.d/roots.conf con el siguiente contenido:

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/salt-stack/IMG/11.png)

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/salt-stack/IMG/12.png)

Reiniciar el servicio del Máster.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/salt-stack/IMG/13.png)

### 4.2 Crear un nuevo estado ###

Crear fichero /srv/salt/base/apache/init.sls:

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/salt-stack/IMG/14.png)

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/salt-stack/IMG/15.png)

### 4.3 Asociar Minions a estados ###

Ir al Máster:

Crear /srv/salt/base/top.sls, donde asociamos a todos los Minions con el estado que acabamos de definir.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/salt-stack/IMG/16.png)

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/salt-stack/IMG/17.png)

### 4.4 Comprobar: estados definidos ###

salt '*' state.show_states, consultar los estados que tenemos definidos para cada Minion:

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/salt-stack/IMG/18.png)

### 4.5 Aplicar el nuevo estado ###

Ir al Master:

Consultar los estados en detalle y verificar que no hay errores en las definiciones.

salt '*' state.show_lowstate

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/salt-stack/IMG/19.png)

salt '*' state.show_highstate

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/salt-stack/IMG/20.png)

salt '*' state.apply apache, para aplicar el nuevo estado en todos los minions. OJO: Esta acción puede tardar un tiempo.

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/salt-stack/IMG/21.png)

![image](https://github.com/christianjmx/ADD_christian/blob/main/TRIM%202/salt-stack/IMG/22.png)

