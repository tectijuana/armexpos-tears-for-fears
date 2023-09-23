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
Ejercicios ......

Estudiante:
Leyva Garay Jocelyn #21210388
Miranda Juarez Paul Emanuel #21210401
Pompa Retana Brandon Hazael #
Espinosa Inzunza Fernando Manuel #
Lopez Rangel Kevin Paul #



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
	

ENTREGA:

	URL del GitHub Classroom, y recuerde arreglar la PORTADA, quitar todos los 
		elementos extras del templete, acomodarlo bien para su presentación 
		solo lo necesario.

	</p>

</pre>
<pre>
	<p aling=left>
	Los registros R0 a R6 en ARM son registros de propósito general:
		• R0 a R3: Son los registros de argumentos y rasguños; R0 y R1 también son los registros de resultados.
		• R4 a R6: Son registros de guardado de llamadas.
		• R7: se utiliza comúnmente como un puntero de marco de pila en el modo Thumb. En el código de 	ensamblaje, 
			puedes ver que después de una llamada a una función, GCC usa R7 para hacer pop a los valores en PC en lugar de LR. 
			Esto no significa que R7 se ponga en PC, sino que ambos registros se sacan de la pila
		• R8 - R10: Son registros generales en la arquitectura ARM,  Estos registros son de 32 bits y se utilizan para 
			almacenar = datos en el procesador,  Los registros R8, R9 y R10 son parte de los registros desagrupados 
			que apuntan al mismo registro físico en todos los modos de funcionamiento.
		
	</p>
</pre>
