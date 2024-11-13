# Práctica 2.7 - Creación y configuración de un escenario de red completo II

## Descripción de la tarea

Crea y configura una red en Cisco Packet Tracer que incluya los siguientes elementos:

- Al menos 5 equipos de escritorio y 5 dispositivos móviles (tablets, portátiles o smartphones).
- Al menos 2 switches para segmentar la red.
- Un router inalámbrico WRT300N.
- Un servidor de FTP para la transferencia de archivos.
- Un servidor de correo electrónico (SMTP/POP3).
- Un servidor de DHCP que asigne dinámicamente las IPs a los equipos que así se indiquen.
- Un servidor WEB.

Requisitos:

- El primer switch servirá para conectar el router con los servidores.
- El segundo switch conectará el primer switch con los equipos de sobremesa.
- La red usará una IP de clase A privada con 8 bits como identificador de red.
- La puerta de enlace predeterminada tendrá como IP la primera disponible de la red.
- Los 4 servidores tendrán configurada su IP con las cuatro inmediatamente posteriores a la del router.
- Los equipos de escritorio tendrán configurada su IP de forma estática a partir de la X.X.X.10/8 (inclusive).
- Los equipos móviles tendrá IP dinámica asignada por el servidor de DHCP.
- El servidor de DHCP asignará como máximo IPs a 50 dispositivos distintos.
- El router tendrá una lista blanca para los dispositivos que se conecten por el punto de acceso inalámbrico.
- El servidor de FTP tendrá 2 usuarios, uno con todos los permisos, y otro con permisos de solo lectura. Comprueba mediante la terminal que los permisos se asignan correctamente.
- El servidor de correo tendrá 2 cuentas de correo para 2 usuarios distintos. Configura cada cuenta en un equipo y haz un envío de un correo electrónico y su posterior respuesta.
- El servidor HTTP mostrará un "¡Hola primero de ASIR!" en su archivo index.html, y se deberá poder acceder desde cualquier dispositivo final de la red.

## Criterios de evaluación

Esta práctica evalúa los criterios de evaluación **a)**, **d)**, **e)** **f)**, y **g)** del **RA2**. Para su corrección se tendrá en cuenta:

1.	Topología de Red Correcta y Conexión de Dispositivos (15%)
    - Implementación de los switches, router, servidores y dispositivos finales según los requisitos.
2. Asignación Correcta de Direccionamiento IP (20%)
    - Uso de una IP privada de clase A con 8 bits de identificador de red.
	- Configuración correcta de la puerta de enlace, servidores, dispositivos de escritorio y móviles según se indica.
3. Configuración del Servidor DHCP (10%)
    - Asignación dinámica de IPs a los dispositivos móviles.
    - Configuración del alcance para un máximo de 50 dispositivos.
4. Configuración del Servidor FTP (10%)
    - Creación de 2 usuarios con los permisos adecuados.
    - Verificación de permisos a través de la terminal.
5. Configuración del Servidor de Correo Electrónico (10%)
    - Creación de 2 cuentas de correo.
    - Envío y respuesta exitosa de correos entre dispositivos.
6. Configuración del Servidor WEB (10%)
    - Personalización del archivo index.html con “¡Hola primero de ASIR!”.
    - Accesibilidad desde cualquier dispositivo final de la red.
7. Configuración del Router Inalámbrico con Lista Blanca (10%)
    - Implementación de la lista blanca para dispositivos conectados vía inalámbrica.
8. Funcionalidad General de la Red y Cumplimiento de Requisitos (15%)
    - Pruebas de conectividad y acceso a los servicios.
    - Cumplimiento de todos los requisitos establecidos en la práctica.


## Entrega de la práctica

Crea un archivo ZIP con el archivo del escenario de Cisco Packet Tracer, y súbelo en el lugar de la plataforma Moodle Centros habilitado para ello, con el siguiente nombre:

**Apellido1Apellido2_Nombre_PAR_UD2_P6.zip**