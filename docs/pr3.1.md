# Práctica 3.1 - Comportamiento del switch

Los switches LAN de capa 2 llevan a cabo los procesos de conmutación y filtrado basándose solamente en la dirección MAC de la capa de enlace de datos (capa 2) del modelo OSI. El switch es completamente transparente para los protocolos de red y las aplicaciones de usuario. Crean una tabla de direcciones MAC que utilizan para tomar decisiones de reenvío y dependen de los routers para pasar datos entre subredes IP independientes.

## Tablas de direcciones MAC

Los switches emplean direcciones MAC para dirigir las comunicaciones de red a través de su estructura al puerto correspondiente hasta el nodo de destino. La estructura del switch son los circuitos integrados y la programación de máquina adjunta que permite controlar los datos a través del switch. El switch debe primero saber qué nodos existen en cada uno de sus puertos para poder definir cuál será el puerto que utilizará para transmitir una trama unicast.

El switch determina cómo manejar las tramas de datos entrantes mediante una tabla de direcciones MAC. El switch genera su tabla de direcciones MAC grabando las direcciones MAC de los nodos que se encuentran conectados en cada uno de sus puertos. Una vez que la dirección MAC de un nodo específico en un puerto determinado queda registrada en la tabla de direcciones, el switch ya sabe enviar el tráfico destinado a ese nodo específico desde el puerto asignado a dicho nodo para posteriores transmisiones.

Cuando un switch recibe una trama de datos entrantes y la dirección MAC de destino no figura en la tabla, éste reenvía la trama a todos los puertos excepto al que la recibió en primer lugar. Cuando el nodo de destino responde, el switch registra la dirección MAC de éste en la tabla de direcciones del campo dirección de origen de la trama. En las redes que cuentan con varios switches interconectados, las tablas de direcciones MAC registran varias direcciones MAC para los puertos que conectan los switches que reflejan los nodos de destino. Generalmente, los puertos de los switches que se utilizan para interconectar dos switches cuentan con varias direcciones MAC registradas en la tabla de direcciones.

## Descripción de la tarea

1. Indica y describe los [métodos de reenvío](https://www.sapalomera.cat/moodlecf/RS/2/course/module1/#1.2.1.3) para conmutar datos entre los puertos de la red: Switching de [almacenamiento y envío (store and fordware)](https://www.sapalomera.cat/moodlecf/RS/2/course/module1/#1.2.1.4) y Switching por [método de corte (cut through)](https://www.sapalomera.cat/moodlecf/RS/2/course/module1/#1.2.1.5).
2. Realiza la [siguiente actividad](https://www.sapalomera.cat/moodlecf/RS/2/course/module1/#1.2.1.6) sobre métodos de reenvío de tramas y entrega una captura con la solución correcta.
3. Realiza la [siguiente actividad](https://www.sapalomera.cat/moodlecf/RS/2/course/module1/#1.2.2.4) sobre dominios y entrega capturas con las soluciones correctas.
4. Enumera y explica brevemente las ventajas de [full-duplex frente a half-duplex](https://www.sapalomera.cat/moodlecf/RS/1/course/module5/5.3.1.3/5.3.1.3.html)
5. Explica qué es [AUTO-MDIX](https://www.sapalomera.cat/moodlecf/RS/1/course/module5/index.html#5.3.1.4).
6. Realiza las siguientes [actividades](https://www.sapalomera.cat/moodlecf/RS/1/course/module5/5.3.1.9/5.3.1.9.html) y resume en qué consiste el comportamiento de un switch (5 escenarios con 5 comportamientos distintos).

## Criterios de evaluación

Esta práctica evalúa todos los criterios de evaluación del **RA3**. Para su corrección se tendrá en cuenta:

- Comprensión y aplicación de conceptos técnicos (40%)
- Análisis y razonamiento lógico (25%)
- Exactitud y completitud de las respuestas (20%)
- Claridad y coherencia en la redacción (10%)
- Uso adecuado de terminología técnica (5%)

## Entrega de la práctica

Contesta a las cuestiones, genera un documento .PDF, y súbelo en el lugar de la plataforma Moodle Centros habilitado para ello, con el siguiente nombre:

**Apellido1Apellido2_Nombre_PAR_UD3_P1.pdf**