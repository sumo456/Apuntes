SEGURETAT ACTIVA: MALWARE||||||||||||||||||||||||||||||||||||||||

 
ATACS CONTRA DADES I APLICACIONS: EL MALWARE
Software que tienec omo finalidad infiltrarse o dañar un ordenador sin el consentimiento de su propietario.

Virus
Gusano
Troiano
SpyWare

OJBETIVOS DE MALWARE

Monitorear y espiar usuarios
Robar informacion
Robar Identidad y credenciales
Destruir datos de los dispositivos conectados y accesibilidades
Conseguir el control de los equipos de forma remota o local
Robar dinero y extorsionar a los usuarios


Virus: Micropgrama que tiene la capacidad de replicarse a si mismo y propagarse infectando otros software.
Gusanos: No dependen de archivos portadores para contaminar sistemas. Realizan copias de si mismos en la memoria RAM a la maxima velocidad posible.
Troiano: Software nocibo con apariencia de prgarama legitimo
Backdoor: Software que permite acceso al sistema del ordenador ignorando el procedimiento normal de autenticacion
Bomba logica: Objetivo destruir los datos de un ordenador o causar otros males de consideracion cuando se cumplen ciertas condiciones.
Spyware: Software recolecta y evia informacion
ADware:Muestra publicidad
Rasnomware: programa qeu restringe el acceso de archivos de un ordenador
Hoaxes: son mensajes engañosos que se difunden masivamente por internet
Rootkit: Software insertado en un rodenador despues de coseguir control en un sistema.

1. DEFECTOS DE SEGURIDAD DEL SOFTWARE
Errores de programacion
Programacion de las aplicaciones de forma no segura

2. CONFIGURACION ERRONIA DEL SISTEMA
Instalacion sin configuracion
Instalacion de servicios sin configuracion
Sistemas sin limitaciones

3. DISEÑO INSEGURO O ERRORES DE USUARIOS
Arrancar des de dispositivos infectados por malware
Carga automatica de codigo html infectado en navegadores
Ejecucion de software que llegan via pendrive

4. CODIGO O USUARIOS CON MAS PRIVILEGIOS DE LA CUENTA
Limitacion de derechjos y cuotas
Utilizar usuarios sin privilegios siempre
Utilizar sudo o run as momentaniamente
Nunca hacer chmod 777 o Todos Control total a sistemas de archivos

5. USO DEL MISMO S.O
Utilizar el mismo S.O  en todos los equipos

6. ANTI-MALWARE
Diseñado para detectar y eliminar si es posible amenazas


FIRMAS DE VIRUS Y MALWARE
Empresas recogen muestras de malware y la analizan en busca de patrones

HEURISTICA

SANDBOX
Mecanismo de seguridad para ejecutar software por separado

REGISTRAR HASH DE FICHEROS

Esta tecnica consiste en generar una base de datos con el hash de todos los ficheros del sistema

CRIPTOGRAFIA|||||||||||||||||||||||||||||||||||||||||

Modelos de cifrado
	Cifrado simetrico: Metodo utilizado des de los inicios de la criptografia
		Solo se utiliza un clave para cifrar y descifrar
	Cifrado asimetrico: Metodo que aparecio en la 2 Guerra mundial

Cifrado Simetrico
Los sistemas clásicos de cifrado no son suficientemente robustos para los
ordenadores actuales. En muy poco tiempo se puede obtener la clave por fuerza sucia. Ejemplos de éstos son:

Algoritmos clasicos
Scytala
César / ROT-13
Sustitución
CHOR
Vigenère

Algoritmos actuales
DES
3DES
RC5
AES
Blowfish
IDEA

Ventajas:
	Asegurar la confidenciaidad
	Rapidez de cifrado y descifrado
	Utrilizacion en comunicaciones interactivas
Desventajas:
	Problemas de intercambio de claves
	No asegura autenticacion, integridad
	Necesita una llave para cada pareja de entidades

Xifrat Asimetric
Uso de dos llaves, llave publica y lalve privada
Confidencialidad: Cifrar con la clave publica
Autenticacion: cifrado con l allave privada

Ventajas:
	Ofrece confidencialidad y autentificacion
	Utilizado para intercambio de claves simetricas de forma segura
Desventajas:
	Mas lento y llaves mas largas
	Mensajes cifrado ocupan mas espacio

Algoritmos actuales:
Diffie-Hellman
RSA
DSA
ElGamal
Criptografia de curva eliptica

Funiones de Hash
Generan un valor de tamaño fijo.
Irreversible
Utilizado par assegurar la integridad de los datos

Ejemplos:
	MD5
	SHA-1
	SHA-2
Usos practicos
	Validar integridad de ficheros
	Gaurdar contraseñas de manera segura
	Firma digital

Cifrado hibrido

Asimetrico para enviar la llave secreta
Simetrico para cifrar los datos
Llave de sesion utilizada solo durante la sesion, interceptarla no servira para otra sesion