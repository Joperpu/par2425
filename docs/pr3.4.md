# Práctica 3.4 - Etherchannel y STP

## Ejercicio 1: Implementación de EtherChannel

### Objetivo:

Configurar EtherChannel en un escenario con enlaces redundantes entre switches para aumentar el ancho de banda y garantizar la redundancia.

### Escenario:

- Dispositivos:
    - 3 Switches (S1, S2 y S3).
	- 2 PCs (PC1 y PC2).
- Conexiones:
	- S1 conectado a S2 a través de 2 enlaces GigabitEthernet.
	- S2 conectado a S3 a través de 2 enlaces FastEthernet.
	- PC1 conectado al switch S1 (puerto Fa0/1).
	- PC2 conectado al switch S3 (puerto Fa0/1).

### Tareas a realizar:
	
1. Configurar EtherChannel en los enlaces entre S1 y S2 usando el protocolo PAgP.
2. Configurar EtherChannel en los enlaces entre S2 y S3 usando el protocolo LACP.
3. Verificar la correcta creación del port-channel en ambos switches.
4. Comprobar la conectividad entre PC1 y PC2 realizando un ping.
5. Configurar el balanceo de carga basado en la dirección MAC de origen en S1 y en la dirección MAC de destino en S3.
6. Verificar la configuración del balanceo de carga.

## Ejercicio 2: Implementación de STP

### Objetivo:

Configurar STP en una red conmutada para prevenir bucles y garantizar la redundancia.

### Escenario:
- Dispositivos:
    - 3 Switches (S1, S2 y S3).
	- 2 PCs (PC1 y PC2).
- Conexiones:
	- S1 conectado a S2 a través de 2 enlaces FastEthernet.
	- S1 conectado a S3 a través de 1 enlace FastEthernet.
	- S2 conectado a S3 a través de 1 enlace FastEthernet.
	- PC1 conectado al switch S2 (puerto Fa0/1).
	- PC2 conectado al switch S3 (puerto Fa0/1).

### Tareas a realizar:
	
1. Configurar S1 como switch raíz primario para la VLAN 1.
2. Configurar S2 como switch raíz secundario para la VLAN 1.
3. Modificar el coste del enlace en S3 para que su puerto Fa0/2 tenga un valor de 10.
4. Modificar la prioridad del puerto Fa0/1 en S2 a un valor de 96.
5. Verificar el estado de STP en todos los switches usando el comando show spanning-tree.
6. Comprobar que los puertos bloqueados y en estado de envío son los esperados para evitar bucles.
7. Realizar una prueba de conectividad mediante ping entre PC1 y PC2 para confirmar que la red es funcional.

## Criterios de evaluación

Esta práctica evalúa todos los criterios de evaluación del **RA3**. Para su corrección se tendrá en cuenta:

Ejercicio 1: Implementación de EtherChannel (50%)
	
1. Configuración correcta de EtherChannel con PAgP entre S1 y S2. (15%)
2. Configuración correcta de EtherChannel con LACP entre S2 y S3. (15%)
3. Verificación de la creación del port-channel y balanceo de carga configurado correctamente. (10%)
4. Comprobación de la conectividad entre PC1 y PC2 mediante ping. (10%)

Ejercicio 2: Implementación de STP (50%)
	
1. Configuración correcta del switch raíz primario en S1. (10%)
2. Configuración correcta del switch raíz secundario en S2. (10%)
3. Modificación del coste del enlace en S3 al valor de 10. (10%)
4. Modificación de la prioridad del puerto Fa0/1 en S2 a 96. (10%)
5. Verificación del estado de STP y comprobación de la conectividad entre PC1 y PC2 mediante ping. (10%)

## Entrega de la práctica

Crea un archivo ZIP con los dos escenarios de Cisco Packet Tracer, y súbelo en el lugar de la plataforma Moodle Centros habilitado para ello, con el siguiente nombre:

**Apellido1Apellido2_Nombre_PAR_UD3_P4.zip**