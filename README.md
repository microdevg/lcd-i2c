# LCD usando I2C.


Este proyecto esta basado en la documentacion del espressif para el manejo del periferico i2c [docs page](https://docs.espressif.com/projects/esp-idf/en/v4.2.3/esp32/api-reference/peripherals/i2c.html).

### Introduccion 
Descripción general
I2C es un protocolo de comunicación semidúplex, síncrono y en serie que permite la coexistencia de múltiples maestros y esclavos en el mismo bus. El bus I2C consta de dos líneas: línea de datos en serie (SDA) y reloj en serie (SCL). Ambas líneas requieren resistencias pull-up.

Con ventajas tales como simplicidad y bajo costo de fabricación, I2C se utiliza principalmente para la comunicación de dispositivos periféricos de baja velocidad en distancias cortas (dentro de un pie).

ESP32 tiene dos controladores I2C (también conocidos como puertos) que son responsables de manejar las comunicaciones en dos buses I2C. Cada controlador I2C puede funcionar como maestro o esclavo. Por ejemplo, un controlador puede actuar como maestro y el otro como esclavo al mismo tiempo.

Características del controlador
El controlador I2C controla las comunicaciones de los dispositivos a través del bus I2C. El controlador admite las siguientes características:

Lectura y escritura de bytes en modo Maestro

modo esclavo

Lectura y escritura en registros que a su vez son leídos/escritos por el maestro.

### Pasos a seguir
En este ejemplo simple vamos a enviar el mensaje de un contador por los pines X e  Y  del I2C. Para ello debemos realizar una seria de pasos:
- Configurar el hardware.
- Configurar los pines para manejar I2C.
- Configurar driver como maestro.
- Envio de mensajes a LCD.


## Imagenes

### Muestras con analizador logico
<img src="imgs/cutecom.png" width="400" />


### Circuito
<img src="imgs/circuito.png" width="400" />


## Requisitos

Para ejecutar estos ejemplos, necesitarás un entorno de desarrollo configurado para la programación de la ESP32, que puede incluir:

- Placa de desarrollo ESP32.
- SDK de Espressif (IDF-ESP32).