# hack-miniblip.github.io

Hackea la MiniBlip, repo para el hackatón CircoLab/BQ/Miniblip

La [miniblip es](https://github.com/bqlabs/miniBLIP) una placa creada
por [BQ](http://github.com/bqlabs) para *wearables* y lo que
surja. Tiene dos botones, 5 botones capacitivos y un array de
leds. Está basada en un Cortex.

## Como comenzar

Conecta la placa a tu USB. Si pulsas el botón cuadrado más cercano al
USB *mientras estás enchufándolo* se pondrá en "modo programación" y aparecerá en tu ordenador como
un USB drive. El fichero firmware.bin será el que habrá que sustituir
por tus propios ficheros cuando los compiles.

## Creando y compilando un fichero.

Se usa el [entorno de desarrollo MBED](http://developer.mbed.org). Lo
primero es darse de alta en el mismo.

Se trabaja sobre el [compilador](https://developer.mbed.org/compiler/)
para compilar los ficheros. El tipo de plataforma es **MBED LPC11U24**,
será la que hay que seleccionar cuando se crea un nuevo proyecto.

Podemos empezar por los
[proyectos del autor de la placa, Alberto Piganti](https://developer.mbed.org/users/pighixxx/),
por ejemplo,
[`blip_rainbow`](https://developer.mbed.org/users/pighixxx/code/blip_rainbow/). Se
importa en el compilador pulsando en "Import this program", recordando
seleccionar la plataforma anterior si te lo pide e importando las
librerías, en este caso PixelLibrary, también si lo pide.

Se compila pulsando en el botón correspondiente y se descarga el
fichero.

## Guardando el fichero.

Se borra el fichero firmware.bin y se arrastra el nuevo fichero a la
placa.

En Linux y OSX hay que
[configurar el sistema para que monte la placa de una forma determinada](https://developer.mbed.org/handbook/Mounting-with-sync),
de forma que grabe en la misma en el momento que se escriba, no en el
momento que se desmonte. Si no no lo grabará.

## Y listo

Al conectar de nuevo el sistema empezará a funcionar el nuevo
programa. 