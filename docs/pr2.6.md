# Práctica 2.6 - Creación y configuración de un escenario de red completo

## Descripción de la tarea

Crea y configura un escenario en Cisco Packet Tracer que incluya los siguientes dispositivos:

- 10 ordenadores de escritorio.
- 5 ordenadores portátiles.
- 2 switches.
- 1 router inalámbrico.
- 1 servidor exclusivo para el servicio de DHCP.
- 1 servidor exclusivo para Web.
- 1 servidor exclusivo para autenticación mediante Radius.

Requisitos:

- La red poseerá una IP de clase C privada.
- La primera IP disponible de la red será asignada a la puerta de enlace predeterminada.
- Los switches segmentarán la red con 5 equipos de escritorio por cada uno de ellos.
- Los servidores de DHCP, Web y Radius poseerán las 3 siguientes IP disponibles, en ese orden, y no serán asignadas dinámicamente.
- Los ordenadores portátiles se conectarán a la red a través de su conexión inalámbrica, para lo cual actuará el servidor Radius, y tendrán IPs estáticas consecutivas, desde la primera disponible para todos los hosts de la red en adelante, tras la asignación de las IPs anteriores.
- Los ordenadores de escritorio tendrán IPs dinámicas que serán asignadas por el servidor de DHCP, no pudiendo encontrarse ninguna de las IPs asignadas anteriormente dentro del rango del DHCP.
- La página _index.html_ del servidor web mostrará el mensaje "¡Hola 1º de ASIR!".
- El servidor Radius tendrá 5 usuarios y contraseñas distintas, para cada equipo portátil que se conecta a la red.
- Comprueba que desde todos los equipos se puede acceder a la página _index.html_ del servidor web.

Documenta todo el proceso con las capturas de pantallas y las explicaciones que consideres necesarias.

## Criterios de evaluación

Esta práctica evalúa los criterios de evaluación **a)**, **d)**, **e)** **f)**, y **g)** del **RA2**. Para su corrección se tendrá en cuenta:

1. Configuración y Diseño de la Red (20%)
    - Creación y conexión correcta de todos los dispositivos (ordenadores, switches, router inalámbrico y servidores).
2. Esquema de Direccionamiento IP y Configuración de DHCP (25%)
    - Asignación correcta de las direcciones IP al gateway y a los servidores (DHCP, Web y Radius).
    - Configuración correcta de direcciones IP estáticas en los ordenadores portátiles.
	- Configuración adecuada del servidor DHCP para asignar IPs a los ordenadores de sobremesa.
3. Configuración del Servidor Radius y Autenticación Inalámbrica (20%)
	- Configuración correcta del servidor Radius con 5 usuarios y contraseñas distintas.
	- Configuración del router inalámbrico para autenticación mediante Radius.
4. Configuración del Servidor Web (15%)
    - Instalación y configuración correcta del servidor web.
    - La página index.html muestra el mensaje “¡Hola 1º de ASIR!”.
5. Verificación y Pruebas (10%)
	- Comprobación de conectividad y acceso exitoso a la página web desde todos los dispositivos.
6. Documentación (10%)
	- Documentación completa del proceso con capturas de pantalla y explicaciones pertinentes.

## Entrega de la práctica

Crea un archivo ZIP con la documentación y el archivo del escenario de Cisco Packet Tracer, y súbelo en el lugar de la plataforma Moodle Centros habilitado para ello, con el siguiente nombre:

**Apellido1Apellido2_Nombre_PAR_UD2_P6.pdf**