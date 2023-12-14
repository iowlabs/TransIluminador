# TransIluminador
Repo para desarrollar un transiluminador.

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
