# Instalacion Debian con Libvirt

## Hola mi nombre es Jhonal y hoy les voy a explicar como instalar una 
## maquina virtual mediante la consola serie.

Para hacerlo mas corto vamos a explicar rapidamente loq ue vamos a 
relaizar a continuacion que no es mas que instalar una maquina virutal 
debian usando la consola serie y las herramientas de libvirt.

Como podemos ver mediente el comando 'virt-install' y sus respectivos 
parametros hemos logrado empezar con la instalacion de la maquina virtual, 
a continuacion se vera los pasos y la configuracion que le daremos.

Como vemos, la MV nos pregunta por el hostname el cual sera bookworm en 
este caso y si nos dimos cuenta nos ha preguntado por el nombre de 
dominio. ¿Cual es la diferencia entre estos dos?

Cuando se habla del nombre de la maquina a nivel de sistema operativo nos 
estamos refiriendo al nombre que lleva para identificarnos dentro de la 
red o internamente. Mientras que el nombre de dominio es el nombre 
completo que la red ve, normalmente este suele ser utilizado para que 
otros equipos se conecten a la maquina mediante el nombre en lugar de una 
IP.

Ahora nos esta preguntando por el usuario root.

Primero tenemos que saber que el usuario root es el que tiene todos los 
poderes del sistema y basicamente pede hacer lo que quiera. Si se decido 
no usar root es porque hay implicaciones como:

1. Tenemos que usar el comando sudo para todo comando critico o de 
administrador.
2. Tenemos una mayor seguridad. Esto quiere decir que un error del 
usuario no rompe el sistema y un intruso no tiene acceso total.
3. No existe una sesion de root, por lo cual inicias sesion como usuario 
normal con privilegios limitados.

En nuestro caso no vamos a querer nada de root por lo cual dejaremos en 
blanco.

Como se pudo observar, despues de ignorar las preguntas para un usuario 
root nos pidio nuestro nombre completo y nuestro nombre de usuario junto a 
la contraseña.

Ahora nos esta preguntando por lo que seria la zona horaria la cual 
seleccionamos madrid y pasamos al siguiente paso que es el particionado de 
disco.

Aqui podemos observar que hay diferentes maneras y las vamos a explicar 
una a una.

En el instalador de debian, el particionado guiado puede usar todo el 
deisco de una sola particion que es lo mas facil pero menos seguro, 
tambien existe LVM para tener volumenes un poco mas flexisbles que se 
pueden redimensionar, añadir cifrados para proteger los datos, o hacerse 
de forma manual para tener un maximo control.

En conclusion cuando mas automatico es, mas facil y cuando mas manues o 
cifrado, mas seguro y flexible pero requiere mas conocimiento.

Nosotros vamos a seleccionar la primera opcion y ahora nos pregunta si 
queremos todos los archivos en una sola particion por lo cual esa es 
nuestra opcion a escoger.

Como podemos apreciar despues seleccionar la opcion recomendada para 
nuevos usuarios nos mostro como se diviio el disco y se ha empezado a 
configurar todo el disco.

Mas adelante nos va a preguntar por el huso horario el cual tiene algunas 
consecuencias si seleccionamos la incorrecta lo cual nos afectara al 
momento de querer automatizar tareas, registrar eventos, sincronizacion 
con otros equipos, etc.

En este apartado nos pregunta por el proxy de paquete.

Un proxy de paquete permite que debian descargue software a traves de un 
servidor intermedario, lo que en un aula reduce el tradico a internet y 
acelera las instalaciones, pero si el proxy esta mal configurada, los 
equipos no podran actualizar ni instalar paquetes.

Mientras que se instalan los paquetes vamos a explicar otras cosas como lo 
que es un servidor SSH.

instalar debian sin interfaz grafica pero con SSH es util para administrar 
servidores ligeros de forma remota o conectar a otros ordenadores, y 
utilidades estandar del sistema facilitan tareas basicas de administarcion 
desde la consola.

Como vemos se ha terminado de bajar los paquetes y hora nos pregunta si 
queremos participar en una encuesta lo cual vamos a pasar de ella.

Aqui estamos en el menu para escoger los entornos que vamos a utilizar 
pero ya que esta maquina no cuenta con el espacio suficiente no se va a 
instalar ninguno, solo instalaremos el SHH y las utilidades del sistema.

Vamos a explicar lo que acaba de aparecer que es el sistema de arranque.

El gestor de arranque mejor conocido como GRUB permite que la computadora 
inice debian y otros sistemas operativos si existen; si no se instala, el 
sistema no prodra arrancar desde el disco y habria que usar un medio 
externo para iniciarlo o repararlo.

En Conclusion:

La instalacion de debian bookworm mediante virt-install en una maquina 
virtual sin entorno grafico  demuestra como se pueede obtener un sistema 
linux funcional, seguro y liviano, totamente manejable desde la linea de 
comandos.

Como podemos ver ya se ha creado la maquina virtual y hemos accedido a 
ella, ahora vamos a usar un comando para saber la cantidad de paquetes 
instalados y otro para saber el espacio que hay en el disco.

Como podemos ver este comando lo que nos muestra son los paquetes 
instalados lo cual esos numero ahi lo que pintan es lo siguiente:

322: los paquetes instalados.
644: Cada linea tiene dos palabras, es decir paquete + estado.
8441: Son los caracteres, la longitud de texto toal que hay.

Ahora vamos con el comando del espacio.

Como podemos ver aqui nos muestra los espacios que tiene el disco. 

Bueno esto seria todo por hoy, hasta la proxima. 
