![](https://s3.amazonaws.com/videos.pentesteracademy.com/videos/badges/low/arm-assembly.png)

Borrar y modificar a su gusto este README, pero antes utilizar estas condiciones de entrega del trabajo.

# Utilizar los dos directorios

- code  - ahi depositar sus programas los ***archivos extensión *.s****  (Source File) algunos autores en x86 de ponen .asm y en otras plataformas ARM compatibles la extension *.elf
- Todo programa lleva su comentario en la parte de arriba, objetivo y nombre del programador minimo.
- images  - de haber algo de pantallas ahi se presentaran, su busca documentarlas en MARKDOWN el código es:

``` ![](images/---archivo.jpg---) recordar que no lleva espacios```



- Programa en MarkDown es inicia con tres tildes * (`) sin espacio, seguido de el lenguaje de programacion, al final del codigo se poner otra vez los mismos tilder..

No se usan espacios en nombres de archivos, usar los nombres estilo camelCase (primera palabra minusculas, mayuscula solo la 1ra letra de cada palabra subsecuente):  ejemplo: sensorHumo, etc.

Suerte.

Att. ![](https://img.icons8.com/color/2x/docker.png)

------

<pre>

	<p align=center>

Tecnológico Nacional de México
Instituto Tecnológico de Tijuana

Departamento de Sistemas y Computación
Ingeniería en Sistemas Computacionales

Semestre:
Febrero - Junio 2022

Materia:
Lenguajes de interfaz

Docente:
M.C. Rene Solis Reyes 

Unidad:
1

Título del trabajo:
Registros

Estudiante:
Leyva Garay Jocelyn #21210388
Miranda Juarez Paul Emanuel #21210401
Pompa Retana Brandon Hazael #21210416
Espinosa Inzunza Fernando Manuel #21210371
Lopez Rangel Kevin Paul #21210392
		



	</p>

</pre>

<pre>

	<p align=left>
	Registros

	ARM tiene 37 registros en total, todos son de 32-bits.
		 1 dedicado al contador de programa PC
		 1 dedicado al registro de estado en curso
		 5 dedicados a salvar el registro de estado de programa
		 30 registros de propósito general
		 Sin embargo, estos están dispuestos en varios bancos, con el banco
	accessible comandado por el modo del procesador. Cada modo puede
	accesar
		 Un conjunto particular r0-r12 registros
		 Uno particular r13 (the stack pointer) y r14 (link register)
		 r15 (contador de programa)
		 cpsr (registro de estado del programa corriendo)
		y modos priviligeados tienen acceso a
		 Un particular spsr (registro de estado salvado del programa)
	</p>

</pre>
<pre>
<p aling=left>
<img src="https://brandlogos.net/wp-content/uploads/2020/09/arm-logo.png">
	Los registros R0 a R6 en ARM son registros de propósito general:
	• R0: Es uno de los registros de propósito general más utilizados en ARM. Puede usarse para almacenar datos temporales 
	y realizar una variedad de operaciones.
		• Argumento y Resultado: En algunas convenciones de llamada a funciones, R0 se utiliza para pasar argumentos a 
		funciones y para almacenar el resultado de una función.

	• R1: Al igual que R0, R1 se usa para almacenar datos temporales y realizar operaciones matemáticas y lógicas.
		• Argumento y Resultado: En algunas convenciones de llamada a funciones, R1 se utiliza para pasar argumentos y para 
		almacenar resultados.

	• R2: Se utiliza como un registro de propósito general para manipulación de datos y cálculos.
		• Argumento y Resultado: En algunas convenciones de llamada a funciones, R2 se usa para pasar argumentos y para
		almacenar resultados de funciones.

	• R3: Al igual que los anteriores, es un registro de propósito general que se utiliza para diversas tareas. Argumento y 
		Resultado: En algunas convenciones de llamada a funciones, R3 se emplea para pasar argumentos y para almacenar 
		resultados.

	Estos registros (R0 al R3) son fundamentales en la programación en ensamblador ARM, ya que son los registros más utilizados
		para operaciones comunes. Dependiendo del contexto y de las convenciones de llamada a funciones utilizadas en un programa
		específico, estos registros pueden tener diferentes roles, como argumentos, resultados o registros temporales.
	
	• R4: se utiliza como un registro de propósito general en el procesador ARM. Puede almacenar datos temporales, realizar cálculos y
		participar en diversas operaciones de procesamiento de datos.
		• Argumento y Resultado: En algunas convenciones de llamada a funciones en lenguaje ensamblador ARM, R4 puede utilizarse 
		para pasar argumentos a una función o para almacenar resultados, dependiendo de la convención específica utilizada en el programa.
		• Preservación de Registros: En algunas situaciones, especialmente al llamar a funciones o subrutinas, el contenido de R4 puede ser
		preservado (guardado) por la función llamada si se espera que mantenga su valor antes y después de la llamada.
		• Direcciones de Memoria: R4 también se puede utilizar para almacenar direcciones de memoria o desplazamientos en el contexto de 
		acceso a memoria.
	
	• R5: Se utiliza como un registro de propósito general en el procesador ARM. Puede almacenar datos temporales, realizar cálculos y participar
		en diversas operaciones de procesamiento de datos.

	• R6: es un registro de propósito general que se utiliza para almacenar datos temporales, realizar operaciones y, en algunas circunstancias,
		para pasar argumentos o almacenar resultados de funciones.

	• R7: se utiliza comúnmente como un puntero de marco de pila en el modo Thumb. En el código de 	ensamblaje, 
		puedes ver que después de una llamada a una función, GCC usa R7 para hacer pop a los valores en PC en lugar de LR. 
		Esto no significa que R7 se ponga en PC, sino que ambos registros se sacan de la pila
		
	• R8 - R10: Los registros R8, R9 y  R10 son parte de los registros desagrupados que apuntan al mismo registro físico en 
		todos los modos de funcionamiento.
		Esto significa que estos registros tienen el mismo valor en todos los modos de ejecución.
		
	• R11: Este registro se puede utilizar para almacenar datos temporales o para realizar cálculos intermedios durante la 
		ejecución de un programa
		
	• R12:  El registro R12 se designa como un registro de uso temporal  Esto significa que se puede utilizar para almacenar 
		datos temporales o para realizar cálculos intermedios durante la ejecución de un programa
		
	• R13: se conoce comúnmente como el registro R13 o SP (Stack Pointer), que es un registro de propósito general utilizado 
		principalmente para realizar seguimiento y gestión de la pila de llamadas.
		
	• R14: se conoce comúnmente como el registro R14 o LR (Link Register), y se utiliza para gestionar las direcciones de 
		retorno de las subrutinas y funciones.
		
	• R15: se conoce como el registro R15 o PC (Program Counter), y es uno de los registros más cruciales en el procesador ARM.
	<img src="https://pic002.cnblogs.com/images/2012/392443/2012040421074226.jpg">
	
	</p>
	
<img src="https://i.pinimg.com/originals/9b/89/85/9b89857e916858b774153a4f0c2e1829.gif">
</pre>
