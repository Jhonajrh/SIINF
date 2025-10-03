# Fundamentos de los sistemas informáticos

Este trabajo tiene como objetivo explicar de manera sencilla los
fundamentos de los sistemas informáticos. Vamos a ver qué es lo que hay
dentro de un ordenador, cómo se organiza, qué piezas lo forman, qué
programas necesita para funcionar y también qué normas debemos seguir
para trabajar con él de manera cómoda y sin riesgos.

---

## 1. Arquitectura de un sistema informático: el modelo Von Neumann

Casi todos los ordenadores actuales siguen el **modelo de Von Neumann**.
Este modelo se inventó hace ya muchas décadas, pero todavía sigue siendo
la base. La idea es dividir el ordenador en tres grandes bloques:

1. **Unidad central de proceso (CPU)**: el cerebro del ordenador, que
   ejecuta las instrucciones.
2. **Memoria**: es como la libreta del ordenador, donde guarda datos y
   programas mientras los usa.
3. **Dispositivos de entrada y salida**: todo lo que usamos para hablar
   con el ordenador, como teclado, ratón, pantalla o impresora.

Lo curioso del modelo es que los **programas se guardan en memoria igual
que los datos**, y eso permite que el procesador pueda leerlos y
ejecutarlos.

---

## 2. Componentes hardware de un sistema informático

El **hardware** son todas las piezas físicas que forman un ordenador.
Podemos abrir la caja y verlas, tocarlas y hasta cambiarlas.

### 1. Microprocesador (CPU)

El microprocesador es un chip diminuto que actúa como cerebro del
ordenador. Está formado por millones o miles de millones de transistores.

Hace tres cosas básicas todo el tiempo:

1. **Buscar** instrucciones en memoria.
2. **Decodificarlas**, es decir, entender qué tiene que hacer.
3. **Ejecutarlas**: sumar, mover datos, comparar números, etc.

Hoy en día los procesadores suelen tener varios **núcleos**, lo que
permite hacer muchas tareas a la vez.

---

### 2. Memoria principal (RAM)

La memoria RAM es donde el ordenador guarda lo que está usando en ese
momento. Es muy rápida, pero **se borra al apagar**.

Un ejemplo claro: si tienes abierto un documento en Word y se apaga el
ordenador sin guardar, lo que estaba en RAM se pierde.

---

### 3. Placa base

La **placa base** conecta todo el hardware. Es como una autopista donde
todas las piezas hablan entre sí.

Partes importantes de la placa:

- **Chipset**: organiza la comunicación entre CPU, memoria y otros
  componentes.
- **Zócalo del procesador**: el sitio exacto donde se coloca la CPU.
- **Ranuras de memoria**: para conectar los módulos de RAM.
- **Ranuras de expansión**: donde se ponen tarjetas gráficas, de sonido,
  etc.
- **BIOS/UEFI**: un programita que se ejecuta nada más encender el
  ordenador.
- **Conectores internos y externos**: cables de discos, puertos USB,
  HDMI, red, audio, etc.

---

### 4. Dispositivos de almacenamiento secundario

Como la RAM se borra, necesitamos sistemas que guarden los datos para
siempre (o al menos hasta que queramos borrarlos):

Tipos:

**Flash:**

- Ejemplos: SSD, pendrives
- Caracteristicas Principales: Muy rápidos, sin partes móviles.

**Magnéticos:**

- Ejemplos: Discos duros (HDD).
- Caracteristicas principales: Más baratos, con platos que giran.

**Ópticos:**

- Ejemplos: CD, DVD, Blu-ray.
- Caracteristicas principales: Hoy casi en desuso, lectura con láser.

---

### 5. Fuente de alimentación

Convierte la electricidad de casa en la energía que necesitan los
componentes del ordenador. Además reparte el voltaje correcto a cada
pieza (no es lo mismo lo que necesita la CPU que un ventilador).

---

### 6. Periféricos

Los periféricos son los dispositivos que usamos para interactuar con el
ordenador.

- **Entrada**: teclado, ratón, escáner, micrófono…
- **Salida**: pantalla, altavoces, impresora…
- **Entrada/Salida**: pantallas táctiles, memorias USB, impresoras
  multifunción.

---

## 3. Controladores de dispositivos (drivers)

Los controladores, o **drivers**, son pequeños programas que permiten
que el sistema operativo hable con cada dispositivo.

Ejemplo: cuando conectas una impresora nueva y Windows “instala el
controlador”, lo que hace es añadir el traductor que permite al sistema
enviar órdenes que la impresora entienda.

---

## 4. Componentes software de un sistema informático

El **software** es lo que da vida al hardware. Sin programas, el
ordenador sería solo una caja con piezas.

### 4.1 Tipos de software

- **De sistema**: programas básicos como los sistemas operativos.
- **De desarrollo**: herramientas para programar (compiladores,
  entornos de desarrollo).
- **De aplicación**: los programas que usamos todos los días (navegador,
  Word, Spotify, juegos…).

### 4.2 El sistema operativo

El **sistema operativo** es el más importante de todos. Su trabajo es:

- Organizar los recursos (CPU, memoria, discos).
- Permitir que los programas funcionen sin preocuparse de cómo se
  maneja el hardware.
- Ofrecer una interfaz (pantalla, iconos, ventanas o consola).

Sin sistema operativo, tendríamos que hablar directamente con la
máquina en código binario.

---

## 5. Proceso de arranque de un sistema informático (POST)

Cuando encendemos un ordenador, no aparece mágicamente Windows, Linux o
Mac. Hay un proceso que ocurre en segundos y que tiene varios pasos:

1. **Encendido** → La corriente llega a la placa base.
2. **BIOS/UEFI** → Se pone en marcha y realiza el **POST (Power-On Self
   Test)**, que comprueba memoria, procesador, teclado, etc.
3. **Carga del gestor de arranque** → Busca un disco que tenga sistema
   operativo y carga un programa especial llamado *bootloader* (ejemplo:
   GRUB en Linux).
4. **Arranque del sistema operativo** → Aquí entra en juego el **kernel**.

El **kernel** es la parte más esencial del sistema operativo.
Podemos imaginarlo como **un intermediario entre los programas y el
hardware**.

- Si un programa quiere usar la memoria, no la coge directamente: **le
  pide permiso al kernel**.
- Si quieres guardar un archivo, no escribes tú en el disco: **el kernel
  lo hace por ti**.
- Si abres el navegador y al mismo tiempo escuchas música, el kernel
  decide **qué parte de la CPU** usa cada aplicación para que no se
  bloquee nada.

En pocas palabras:
El kernel es el **jefe que organiza todos los recursos** del
ordenador (procesador, memoria, dispositivos) y se asegura de que todo
funcione sin chocar.

Sin kernel, un sistema operativo no existiría, porque los programas no
podrían comunicarse con el hardware.

---

## 6. Normas de seguridad y prevención de riesgos laborales

Trabajar con ordenadores parece inofensivo, pero si lo hacemos muchas
horas sin cuidado, podemos acabar con dolores de espalda, vista cansada
o problemas en las muñecas.

Algunas normas básicas:

- **Pantalla**: debe estar a la altura de los ojos y a unos 50–60 cm de
  distancia.
- **Teclado y ratón**: se deben usar con las muñecas rectas, sin
  forzarlas.
- **Mesa y silla**: la silla debe tener respaldo, apoyar la espalda y
  permitir que los pies lleguen al suelo.
- **Entorno**: buena iluminación, sin reflejos en la pantalla y con
  cables recogidos para evitar tropiezos.
- **Pausas**: conviene levantarse cada hora, mover brazos y piernas y
  descansar la vista mirando a lo lejos.

---

