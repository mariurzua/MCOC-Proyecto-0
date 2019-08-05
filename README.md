# MCOC-Proyecto-0

from decimal import Decimal
from fractions import Fractions

Fractions.from_float(0,1)

(0,1).as.integer_ratio()

Decimal.from_float(0,1)

Format(Decimal.from_float(0,1),'.17')


# No pude descargar python (cambie de computador y me cuesta mucho realmente lo intenté), pero basandome en lo investigado con los videos e internet esto es lo que haría de código, donde es posible ver como los comandos Decimal y Fraction pueden interferir en el fenómeno de los puntos flotantes. Al trabajar con el n° "0,1", es posible notar que este se puede conservar lo más cercano a la exactitud como fracción (mediante Fraction o .as.interger_ratio). Al usar la transfornación utilizando el comando Decimal.from_float es posible notar que el 0,1 se ve alterado. Es dificil que se interprete exactamente el 0,1 como 1/10, por lo que la computadora procede a hacer un recorte generalmente como se ve en la última línea, donde se conservan 17 dígitos significativos que es lo que comunmente se hace.


# OUTPUT

OUTPUT DE LA CONSOLA:

Fraction(3602879701896397, 36028797018963968)

(3602879701896397, 36028797018963968)

Decimal('0.1000000000000000055511151231257827021181583404541015625')

'0.10000000000000001'

# Cabe considerar que cada n° en un sistema binario se escribe como una composición signo-exponente-mantissa, donde el signo es 0 para un (+) y 1 para un (-), el exponente se da por la suma de 127 + elevación del 2 y la mantissa reprsenta el n° que n se multiplicará por el exponente de el n° de bits (según el video). Por eso, las aplicaciones aritméticas se complican al ser números flotantes, pues si este no queda expresado como fracción, piderde poco a poco la exactitud. Según este ejemplo se trunca considerando una gran cantidad de números significativos para conservar algo la exactitud, facilitando los cálculos.
