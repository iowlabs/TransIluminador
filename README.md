# TransIluminador

Un transiluminador es un instrumento utilizado en experimentos de biología molecular principalmente en procesos de electroforesis en aplicaciones de PCR, clonación, secuenciación o detección de ADN. Su principio se basa en transmitir luz de longitud e intensidad específica a travez de una muestra, lo cual permite visualizar proteinas específicas o ADN.

Para efectos de la instrumentación, consiste en un dispositivo que controla una gran cantidad de LEDs. De este modo, el dipositivo debe encargarse de generar los voltajes de operación y la corriente de los LEDs. Las variables objetivo para ser controladas son:

- voltaje de operación.
- Intensidad de iluminación.
- Tiempo de exposición.

En algunos dispositivos más complejos existen variables como tipos de curva de iluminación, o algunos cuentan con cámaras para la obtención de imagenes en el dispositivo mismo.
asdavsd


## Requisitos del dispositivo.

El dispositivo a desarrollar debe contar con las siguientes caracteristicas:

1. Alimentación de entrada de 12V. De esto se desprende que el dispositivo debe contar con un regulador DCDC tipo boost para los LEDs.

2. Capacidad de controlar diferentes configuraciónes de LEDs de salida.

3. Control de intensidad de los LEDs por medio de un control lineal de corriente.

4. Driver de corriente de hasta 1A por canal.

4. Capacidad para controlar de forma simultanea 2 canales.

5. Lazo de control para monitoreo y calibración de intensidad luminica.

6. Microcontrolador integrado.

7. Modo de operación manual, stand-alone con curvas pre-configuradas o modo de conexión a un host( pc o web app).

8. Monitoreo de la temperatura de los LEDs y sensor de temperatura externo.

9. Interfaz de usuario por medio de panel y pantalla OLED.

## Revisión del componentes.

Led driver de corriente ajustable

Modulo: LD06AJSA

Amazon: https://www.amazon.com/Adjustable-Current-Driver-30-1500mA-Constant/dp/B07S9C5QF1
Aliexpress: https://es.aliexpress.com/item/32848783838.html?gatewayAdapt=glo2esp

Datasheet no disponible, por observación es un potenciometro y una resistencia de 2.2k aparentemente
Parecido a ejemplos del datasheet de CN5711

Utiliza un CN5711

Datasheet: https://html.alldatasheet.com/html-pdf/1133252/CONSONANCE/CN5711/1403/2/CN5711.html

Otra opción pero más estrecho es NSI50150ADT4G controla entre 150 - 350 mA, 50V Vak max

Datasheet: https://www.onsemi.com/pdf/datasheet/nsi50150ad-d.pdf

Otra opción en rango similar al anterior es MAX16815 35mA - 100 mA
o MAX 16828 35mA - 200 mA
Voltaje de entrada entre 6.5 - 40 V

Datasheet: https://www.analog.com/media/en/technical-documentation/data-sheets/MAX16815-MAX16828.pdf

Existe la posibilidad de hacer una fuente de corriente con 2 PNP y 2 resistencias, la corriente resultante sera producto de ambas resistencias, se puede utilizar una entrada logica o directa para el funcionamiento, se puede reemplazar una ressitencia con un potenciometro y conseguir una fuente variable
Revisar archivo Modulo de corriente.asc
