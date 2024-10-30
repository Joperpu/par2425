# Práctica 2.4 - Broadcast o difusión en las redes LAN

La difusión es imprescindible en las redes LAN. Cuando un host quiere comunicarse con otro dentro de la misma red utiliza el broadcast o difusión para localizarlo. No se necesita la puerta de enlace o el router. Para demostrar el proceso, a continuación se explica el proceso del ping entre dos equipos dentro de la misma red local.

## Dominio de colisión

Un dominio de colisión es un grupo de dispositivos conectados al mismo medio físico, de tal manera que si dos dispositivos acceden al medio al mismo tiempo, el resultado será una colisión entre las dos señales. Como resultado de estas colisiones se produce un consumo inadecuado de recursos y de ancho de banda.

En las redes antiguas con topología en bus, y en las que hacen uso de hubs, el medio se comparte, por lo que se producen colisiones. Cuanto menor sea la cantidad de dispositivos afectados a un dominio de colisión mejor es el desempeño de la red.
Hay que evitar, por tanto, los dominios de colisión, y dentro de ellos, mejor que sean pequeños: pocos dispositivos.

## Dominio de broadcast

Grupo de dispositivos de la red que envían y reciben mensajes de difusión entre ellos. Una cantidad inapropiada de estos mensajes de difusión (broadcast) provocara un bajo rendimiento en la red, una cantidad exagerada (tormenta de broadcast) dará como resultado el mal funcionamiento de la red hasta tal punto de poder dejarla completamente congestionada.

## Hubs
El hub fue el primer dispositivo central de la topología en estrella. Recibe datos y los hace llegar a todos los dispositivos que tiene conectados (hosts), lo hace transmitiendo en modo semidúplex (ambas direcciones, pero no a la misma vez).

Los hubs o concentradores tienen un único dominio de colisión que incluye todos los dispositivos de red conectados. Eso quiere decir que si dos equipos provocan una colisión en un segmento asociado a un puerto del hubs, todos los demás dispositivos aun estando en diferentes puertos se verán afectados. De igual manera se verían afectados si una estación envía un broadcast, debido a que un hub también tiene un solo dominio de difusión. 


## Ping entre dos host dentro de la misma red local

Cuando la comunicación se realiza entre dos hosts de la misma red la puerta de enlace no se ve involucrada. Supongamos un ping entre dos equipos de una LAN:

- El equipo emisor del ping detecta que el destino está dentro de la misma red. Lo averigua mediante  operaciones binarias:
    - AND(IP_destino, Máscara) 
    - AND(IP_origen, Máscara)
    - Si coinciden con la dirección de red del equipo local significa que están en la misma red IP o red lógica
- El ICMP (capa de red) solicita a la capa inferior que envíe la trama. Se necesita la MAC de destino para encapsular la trama. Si no se tiene (no aparece en arp -a) se usa el protocolo ARP.
- El protocolo ARP 
    - Origen: pregunta a toda la red (request IP)
    - Destino: contesta con su dirección MAC. 
    - Origen: Se actualiza la tabla de MACs del origen
- Ya con la MAC destino:
    - echo request se encapsula en la trama
    - echo reply vuelve

## Descripción de la tarea

Responde a las siguientes preguntas y documenta aquello que sea necesario. Utiliza el modo simulación de Cisco Packet Tracer para las capturas de pantalla de los protocolos.

<center>![Escenario de Cisco Packet Tracer](assets/images/ud2/img33.png)</center>

1. Realiza el Packet Tracer del escenario que se muestra (lo entregarás cuando finalices la tarea). La dirección de red es la 10.0.0.0, y las IPs de los distintos dispositivos son consecutivas desde la primera disponible.
2. Crea una PDU simple que envía un ping del PC de la izquierda al de la derecha. Usa el icono "Add Simple PDU" (el sobre cerrado) arriba a la derecha. Pincha primero en el origen y después en el destino del ping.
3. Usa arp -d para limpiar la cache de las resoluciones arp del equipo origen. Así nos aseguramos de que se va a preguntar a toda la red por la MAC del equipo destino.
4. Entra en el modo simulación, limpia todos los protocolos y añade sólo los protocolos ARP e ICMP.
5. ¿Cuál es el dominio de difusión o de broadcast en el escenario? Envía una captura de pantalla de Cisco Packet Tracer que lo demuestre e indica el protocolo que lo usa y para qué.
6. Indica el escenario y la trama donde se realiza la resolución ARP. En el modelo OSI marca la capa donde se realiza y captura de pantalla. Indica:
    - Capa donde se realiza la resolución ARP.
    - Dirección IP por la que se preguntaba.
    - Dirección MAC devuelta.
7. Nada más solucionarse el problema de la MAC mediante el broadcast, ¿cuál es la siguiente trama que se envía?
8. Repite la simulación. Ya no se realizará el broadcast. Explica por qué.

## Criterios de calificación

Esta práctica evalúa los criterios de evaluación **a)**, **d)**, **e)** **f)**, y **g)** del **RA2**. Para su corrección se tendrá en cuenta:

1. Configuración del escenario en Packet Tracer (20%)
    - Creación correcta del escenario tal como se muestra en la imagen proporcionada.
	- Inclusión de la dirección de red indicada.
	- Añadir el nombre del estudiante en el escenario.
2. Creación y ejecución de la PDU simple y configuración de la simulación (25%)
	- Creación correcta de una PDU simple que envía un ping desde el PC de la izquierda al de la derecha utilizando el ícono “Add Simple PDU”.
	- Uso del comando arp -d para limpiar la caché ARP del equipo origen.
	- Configuración del modo simulación, eliminando todos los protocolos y añadiendo solo ARP e ICMP.
3. Identificación y demostración del dominio de difusión (20%)
	- Correcta identificación del dominio de difusión en el escenario.
	- Envío de una captura de pantalla de Cisco Packet Tracer que lo demuestre.
	- Indicación del protocolo que utiliza el dominio de difusión y explicación de su propósito.
4. Análisis del proceso de resolución ARP (20%)
	- Identificación del escenario y la trama donde se realiza la resolución ARP.
	- Indicación de la capa del modelo OSI donde se realiza la resolución ARP, acompañada de una captura de pantalla.
	- Especificación de:
	    - La capa donde se realiza la resolución ARP.
	    - La dirección IP consultada.
	    - La dirección MAC devuelta.
5. Explicación de la ausencia de broadcast en la repetición de la simulación (15%)
	- Repetición correcta de la simulación sin que se realice el broadcast.
	- Explicación clara de por qué ya no se realiza el broadcast, demostrando comprensión del funcionamiento de la caché ARP y su impacto en la comunicación en redes.

## Entrega de la práctica

Crea un archivo ZIP con el PDF y el archivo del escenario de Cisco Packet Tracer, y súbelo en el lugar de la plataforma Moodle Centros habilitado para ello, con el siguiente nombre:

**Apellido1Apellido2_Nombre_PAR_UD2_P4.pdf**

