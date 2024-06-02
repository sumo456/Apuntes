FIREWALLS I SEGURETAT PERIMETRAL
<p align="center">
<img src="imgs/seguretat-perimetral-firewalls-16bd7db6.png" width="600" />
</p>

Conceptos previos:
IP, máscara, gateway, DNS:

    IP: Dirección que identifica un dispositivo en una red.
    Máscara de subred: Determina qué parte de la IP corresponde a la red y cuál a los hosts.
    Gateway: Dispositivo que conecta una red local con otra red.
    DNS: Servicio que traduce nombres de dominio a direcciones IP.

Mapas de red lógico:

    Representación visual de una red, mostrando dispositivos y conexiones.
    Herramientas para dibujar: Microsoft Visio, Lucidchart, etc.

Tabla de rutas:

    Información que permite a los routers determinar la mejor ruta para enviar datos.

Segmentación de red:

    Dividir una red grande en subredes más pequeñas para mejorar la gestión y la seguridad.

Protocolos de red y modelo OSI:

    Modelo OSI: Estructura en capas que describe las funciones de una red.
    Ejemplo de burocracia: Cada capa del modelo OSI realiza una función específica, similar a un departamento en una empresa.

Firewalls y seguridad perimetral
Medidas de seguridad perimetral:

    Firewall: Dispositivo que bloquea el tráfico no autorizado y permite el autorizado.
    DMZ (Zona Desmilitarizada): Segmento de red donde se ubican servidores públicos.
    IDS (Sistema de Detección de Intrusos) y IPS (Sistema de Prevención de Intrusos): Dispositivos que monitorean la red para detectar y/o bloquear actividades maliciosas.
    Pasarelas antivirus y antispam: Filtran tráfico malicioso.
    Honeypots: Sistemas diseñados para atraer y analizar ataques.

Tipos de firewall:

    Implementación:
        Hardware: Más caros y eficientes, dedicados exclusivamente a funciones de firewall.
        Software: Más económicos, pueden instalarse en hardware general.

    Ubicación:
        Corporativos o de red: Entre redes LAN y WAN.
        Basados en host (personales): Protegen un solo dispositivo.

    Comportamiento y nivel del modelo OSI:
        Firewalls de paquetes (Packet filter): Trabajan en las capas 3 (Red) y 4 (Transporte).
        Firewalls con control de estado (Stateful): Mantienen información sobre conexiones activas.
        Firewalls de nivel de aplicación (Application Layer): Analizan el tráfico en la capa 7 (Aplicación).

Limitaciones de los firewalls:

    No pueden proteger contra ataques internos, negligencia de usuarios, ingeniería social, ni malware en archivos internos.

Configuración de firewalls:

    Política permisiva: Permitir todo el tráfico excepto el explícitamente bloqueado.
    Política restrictiva: Bloquear todo el tráfico excepto el explícitamente permitido.

Arquitecturas de seguridad con firewalls:

    Arquitectura de 1 router:
        Usado en redes pequeñas/domésticas.
        Permite todo el tráfico de salida y bloquea el de entrada no autorizado.

    DMZ de host (Bastión):
        El tráfico externo se dirige a un único host (bastión).
        Menos seguro que una DMZ física.

    Dual Homed Host (o Gateway):
        Un host bastión intercepta todo el tráfico entre la red interna y externa.
        No hay reenvío de tráfico directo entre redes LAN y WAN.

    DMZ con un solo firewall (3-legged model):
        Firewall con tres interfaces de red: externa, DMZ e interna.
        Todo el tráfico debe pasar por el firewall.

    DMZ con dos firewalls:
        Dos firewalls separan las redes externa, DMZ e interna.
        Mayor seguridad, especialmente si los firewalls son de diferentes fabricantes.

IDS y IPS:

    IDS (Sistema de Detección de Intrusos):
        Monitoriza el tráfico de la red y genera alertas ante posibles ataques.
        Tipos: Network IDS (NIDS) y Host IDS (HIDS).

    IPS (Sistema de Prevención de Intrusos):
        Similar al IDS, pero también puede bloquear el tráfico malicioso.
        Más avanzado y reactivo comparado con los IDS.

Ubicación de los IDS:

    Detrás/delante del firewall: Solo detecta ataques externos.
    En un puerto de inspección del switch (mirror port): Puede monitorear todo el tráfico, pero puede generar mucho tráfico en el IDS.
    Usando un TAP (Test Access Point): Replica la comunicación para análisis sin afectar la red original.



Inventario y Monitorización del Tráfico de Redes
Inventario de Activos

Un administrador de red debe conocer el sistema, documentando la red para la administración y la seguridad. Es esencial saber:

    Dónde actualizar el software.
    Detectar bajadas de rendimiento.
    Controlar la actividad de la red.

Documentación de la Red:

    Diseño físico de la red: Ubicación de dispositivos y cableado en el plano del edificio.
    Diseño lógico de la red: Conexiones entre dispositivos, incluyendo configuración de red (IP, nombre de host, servicios).
    Esquema de direccionamiento IP: Tabla con nombres, direcciones IP, máscara de red, Gateway, DNS, y MAC.
    Copias de seguridad de configuraciones de dispositivos: Guardar configuración de routers, firewalls, switches.
    Seguimiento básico de la red: Documentar el funcionamiento actual para comparar en caso de problemas.

Seguimiento de Actualizaciones:
Actualizar hardware, contratar personal, instalar software, etc., detectando anomalías y degradación del sistema.
Inventario de la Red

El inventario permite:

    Saber qué hacen los usuarios.
    Conocer programas instalados y actualizaciones.
    Evaluar características del hardware.
    Determinar si se necesita nuevo hardware.

Programas de Inventario:

    Inventario de activos (computadoras, monitores, impresoras).
    Vista detallada de activos, mapa lógico.
    Historial de modificaciones.
    Administración de sistemas operativos y software.
    Gestión de componentes internos y conexiones de red.

Funcionamiento:
Modo cliente/servidor con un programa de gestión centralizado y un agente informador en cada equipo, o usando administración remota (SSH, SNMP).

Ejemplos:

    OCS Inventory: Programa de código abierto para escanear e inventariar dispositivos.
    GLPI: Programa de gestión de inventario de código abierto.

Sniffers (Analizadores de Protocolos)

Los sniffers inspeccionan el contenido de tramas en la red, en modo interactivo (tiempo real) o no interactivo (análisis forense). Las tarjetas de red en modo promiscuo aceptan todas las tramas, no solo las destinadas a ellas.

Funciones:

    Visualización y filtrado de tramas en tiempo real.
    Guardar y recuperar capturas (pcap).
    Reconstrucción de sesiones TCP.

Utilidad:

    Educativa.
    Depuración de aplicaciones de red.
    Análisis forense.
    Detección de comportamientos anómalos.
    Detectar configuraciones incorrectas y ataques (DoS, ARP poisoning, MiTM).

Ejemplos:

    Tcpdump, Wireshark, Tshark: Analizadores de protocolos.
    Etherape, Ettercap, Bettercap, Kismet: Monitorización y análisis de red.

Analizadores de PCAP

Las herramientas de captura y análisis de paquetes utilizan el formato "pcap" para guardar el tráfico.

Ejemplos:

    Tcpextract, Xplico, Network Miner, ChaosReader, Argus: Herramientas para extraer y analizar datos de capturas pcap.

Monitorización de Servicios y Servidores

Además de conocer los dispositivos en la red, es vital saber su rendimiento y estado.

Ejemplos:

    NTOP: Monitoriza en tiempo real usuarios y programas que consumen más recursos.
    Nagios: Monitoriza servicios, muestra datos activos y notifica caídas de servicios.