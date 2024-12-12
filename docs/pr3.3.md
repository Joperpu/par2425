# Práctica 3.3 - Seguridad de puertos

## Descripción de la tarea

En esta práctica, debes configurar un switch en Cisco Packet Tracer aplicando medidas de seguridad enfocadas en el acceso y la protección de puertos. Partiendo de un escenario nuevo, deberás entregar el archivo del proyecto con la configuración realizada. No se requiere un informe escrito, pero el escenario debe cumplir con los criterios detallados a continuación.

1. Acceso seguro al switch:
    - Configurar acceso por consola protegido mediante usuario y contraseña.
    - Establecer un mensaje de bienvenida (banner) de seguridad visible al acceder al switch.
    - Configurar acceso remoto seguro a través de SSH, deshabilitando el acceso Telnet.
2. Seguridad de puertos:
    - Puerto con dirección MAC estática: Configurar un puerto para permitir únicamente un dispositivo con una dirección MAC específica.
    - Puerto con MAC sticky: Configurar un puerto con aprendizaje dinámico persistente (sticky), para que las direcciones detectadas se conviertan en seguras y persistentes.
    - Puerto con violación configurada: Configurar un puerto para responder ante violaciones de seguridad usando uno de los siguientes modos:
        - **Protect**: Descartar tramas no autorizadas sin alertar.
        - **Restrict**: Descartar tramas no autorizadas con alertas.
        - **Shutdown**: Deshabilitar el puerto tras una violación.
3. Habilitación y deshabilitación de puertos:
    - Deshabilitar todos los puertos que no estén en uso, excepto los configurados con seguridad de puerto.
4. Pruebas de funcionalidad en el escenario:
    - El escenario debe incluir dispositivos conectados a los puertos configurados para demostrar el cumplimiento de los objetivos:
        - Dispositivos autorizados conectados a los puertos configurados.
        - Al menos un intento de conexión de un dispositivo no autorizado en el puerto configurado para violación.

### Dispositivos del escenario y conexiones

1. Switch (1):
    - Configurar como centro de la red para aplicar la seguridad de puertos.
2. Dispositivos finales:
    - PC1: Conectar al puerto configurado con dirección MAC estática. Utilizar una dirección MAC predeterminada del PC.
    - PC2: Conectar al puerto configurado con MAC sticky. La dirección MAC se aprenderá automáticamente al establecer la conexión.
    - PC3: Utilizar como dispositivo no autorizado para probar las violaciones de seguridad. Conectar al puerto configurado con violaciones y validar el comportamiento según el modo seleccionado.
3. Dispositivos de administración:
    - Servidor: Utilizar para probar el acceso SSH al switch y validar la configuración de gestión remota.
4. Conexiones:
    - Conectar cada dispositivo final a un puerto diferente del switch. Por ejemplo:
        - PC1 → FastEthernet 0/1.
        - PC2 → FastEthernet 0/2.
        - PC3 → FastEthernet 0/3 (temporal para probar violaciones de seguridad).

## Criterios de evaluación

Esta práctica evalúa todos los criterios de evaluación del **RA3**. Para su corrección se tendrá en cuenta:

- Acceso seguro al switch (20%):
    - Configuración de acceso por consola y SSH.
    - Inclusión de un banner de seguridad.
- Seguridad de puertos (50%):
    - Puerto con MAC estática correctamente configurado.
    - Puerto con MAC sticky correctamente configurado.
    - Puerto con violación configurada en modo Protect, Restrict o Shutdown.
- Habilitación y deshabilitación de puertos (20%):
    - Todos los puertos no utilizados deben estar deshabilitados.
- Pruebas de funcionalidad (10%):
    - Escenario que muestre dispositivos autorizados y no autorizados conectados según lo indicado en la descripción.

## Entrega de la práctica

Crea un archivo ZIP con el archivo del escenario de Cisco Packet Tracer, y súbelo en el lugar de la plataforma Moodle Centros habilitado para ello, con el siguiente nombre:

**Apellido1Apellido2_Nombre_PAR_UD3_P3.zip**