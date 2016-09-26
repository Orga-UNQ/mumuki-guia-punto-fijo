### Idea

Ya hemos charlado sobre los pesos de los digitos en decimal. Por ejemplo, si la cadena 16 vale “dieciséis” entonces, cada dígito tiene su peso relacionado a la base:

| 1 | 6|
|---|---|
|10^1|10^0|

Ahora bien, ¿cómo pensamos los pesos si escribimos la cadena  ```1,6``` (“uno coma seis”)? Los pesos de los digitos son algo mas chicos:


| 1 | 6|
|---|---|
|10^0|0,1|

Demos un paso mas: ¿cuánto pesan los dígitos en la cadena  ```0,16``` (“cero coma dieciséis”)? 

| 0  | 1 | 6  |
|----|---|----|
|10^0|0,1|0,01|


¿Cómo podemos usar esta idea para representar **números no enteros** en binario?

### Coma fija

La coma, en el sistema decimal, establece una posición para los pesos de los dígitos. Por ejemplo: 

* ```16 = 1 * 10 ^1 + 6* 10 ^0```
* ```1,6 =1 * 10 ^-0 + 6* 10 ^-1```


Es decir que tenemos los pesos de la siguiente manera: 10^1  , 10^0, 10^-1, 10^-2
Y esto puede ser trasladado al sistema binario : 2^1  , 2^0, 2^-1, 2^-2

Entonces la interpretación de ```11,1``` es  **2^1 + 2^0 + 2^-1**

Veamos otro ejemplo: ¿Que obtengo al interpretar 0,1?  **2^-1**

Uno mas: ¿Que obtengo al interpretar 0,11?  **2^-1+2^-2**

De esta manera, encontramos un método para poder darle **valores fraccionarios** a cadenas binarias, el problema que tenemos que en binario no podemos escribir la coma.

#### Sistema de punto fijo

Un **sistema de punto fijo** es un sistema de numeración binario donde se establece una **posición fija para la coma fraccionaria**. Es decir que la coma se asume en un lugar fijo y por lo tanto no es necesario escribirla. Entonces es necesario acordar su posición para todas las operaciones con el sistema (representacion, interpretación, aritmética) 

La notacion de un sistema en punto fijo sin signo es: **BSS(n,m)**, donde n es la cantidad de bits en total, de los cuales m son fraccionarios. Por ejemplo, BSS(5,3) indica que a las cadenas de 5 bits se les consideran 3 bits fraccionarios (y por lo tanto 2 enteros). En este sistema, la interpretación de la cadena ```11111``` es:  **2^1 + 2^0 + 2^-1 + 2^-2+ 2^-3**



#### A trabajar

> Interprete la cadena: 11100 en SM(5,2)