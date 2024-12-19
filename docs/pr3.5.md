# Práctica 3.5 (No evaluable) - EtherChannel y STP

## Ejercicio 1

Dado el [siguiente escenario de Cisco Packet Tracer](assets/pr3.5-ej1.pka), realiza las siguientes configuraciones:

- Switch0:
    - Acceder por el puerto de consola y configura un usuario y contraseña.
    - Configura el mensaje MOTD con tu nombre y apellidos.
    - Configura el acceso a través de SSH.

- Laptop0:
    - Conecta por SSH al Switch0.

- EtherChannel: 
    - Configura la agregación de puertos entre el Switch0 y el Switch1.
    - Crea el canal 1 con los 4 interfaces del escenario.
    - Cambia el balanceo de carga por defecto al que consideres más correcto.

- Switch1:
    - MAC segura estática:
        - Al puerto fa0/1 solo puede conectarse el servidor. El intento de conexión por parte de otro dispositivo tiene que provocar la desactivación del puerto.
    - MAC segura persistente:
        - El puerto fa0/2 admite como máximo 1 dirección MAC segura persistente. La dirección del servidor será aprendida por el switch.
    - Inhabilita todos los puertos qu no se utilizan.
    - Guarda la configuración del switch.

## Ejercicio 2

Dado el [siguiente escenario de Cisco Packet Tracer](assets/pr3.5-ej2.pka), realiza las siguientes configuraciones:

 - Localiza la raíz que se genera de forma automática y cámbiale el nombre de host a "raiz-tuNombre".
 - Estable el Switch0 raíz primaria. Indica en una nota por qué es el switch idóneo para ello.
 - Establece el Switch3 como raíz secundaria.
 - Activa el enlace entre el Switch0 y el Switch4 para que este último alcance la raíz directamente por el puerto fa0/5.