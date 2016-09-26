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
Y esto puede ser trasladado al sistema binario
Creamos un puente con el sistema binario
2^1  , 2^0, 2^-1, 2^-2
Entonces la interpretación de 11,0 es 
2^1 + 2^0 + 2^-1
¿Que obtengo al interpretar 1,1?
¿Y 0,11?
Encontramos un método para poder darle valores a cadenas binarias con fracciones, el problema que tenemos que en binario no podemos escribir la coma.

#### A trabajar


> interprete la cadena: 11100 en SM(3,2)