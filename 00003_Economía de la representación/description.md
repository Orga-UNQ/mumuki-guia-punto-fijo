### Mil veces y una mas...

... hemos hecho economía del conocimiento, y esta no será la excepción.  Combinaremos nuestros dos ingredientes mas usados:

* Representación en BSS
* Dualidad entre interpretación y representación

Veamos cual es el sentido de esto. Si **para interpretar dividimos por 2^n**, buscando escalar a algo mas pequeño, entonces ahora debemos **multiplicar por 2^n** para escalar a algo las grande, buscando obtener un valor entero.

Consideremos por ejemplo el sistema BSS(2,1) para representar el valor 0,5. Sabemos que no podemos calcular **Rbss(0,5)** porque el mecanismo de representación no está preparado para valores no enteros. Entonces primero es necesario conseguir un entero, pero no cualquier entero, sino aquel correspondiente en el sistema BSS(2).

!["BSS(2,1)"](https://raw.githubusercontent.com/Orga-UNQ/mumuki-guia-punto-fijo/master/images/BSS.2.1.png "BSS(2,1)")


Entonces, los pasos son:

1. Llevar el valor X a un entero: **X' = X * 2^n**. En este ejemplo:  **X' = 0,5 * 2^1 = 1**
2. Representar X' en bss: **Rbss(X')**. En este ejemplo: **Rbss(1)=01**

### Poniendo en práctica

¿Cual es la cadena que representa el valor 0,5 en el sistema BSS(3,1)?

