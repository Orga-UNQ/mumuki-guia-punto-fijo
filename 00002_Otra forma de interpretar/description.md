### Si de economía se trata...

... entonces a nuestro juego nos llamaron!

¿Cómo es posible replantear la interpretación vista para punto fijo reusando la intepretación de los sistemas enteros?

Veamos la relación entre los pesos

|Sistema| | | | | | |
|---|---|---|---|---|---|---|---|
| BSS(5)  | 2^4 | 2^3| 2^2|2^1|2^0|,| 
| BSS(5,1)| 2^3 | 2^2|2^1|2^0|,| 2^-1|
| BSS(5,2)|   2^2|2^1|2^0|,|2^-1|2^-2| 

El **bit mas significativo** en BSS(5,2) pesa 2^2, mientras que en BSS(5) pesa 2^4, o sea (2^2)*2^2.
Lo mismo ocurre con el **bit menos significativo**: en  BSS(5,2) pesa 2^-2, mientras que en BSS(5) pesa 2^0, o sea (2^-2)*2^2=.

Economizar conocimentos previos: 
1. Interpretar el número como en BSS() 

  * IBSS(00001)=2^0
  * IBSS(00100)=2^2
  * IBSS(00101)=2^2 + 2^0

2. dividir por 2^m, siendo m la cantidad de bits fraccionarios
 
 * IBSS(5,2)(00001)=2^0 / 2^2 = 2^-2 = 0,25
 * IBSS(5,2)(00100)=2^2 / 2^2 = 2^0 = 1
 * IBSS(5,2)(00101)= (2^2+2^0) / 2^2 = (2^2 / 2^2) + (2^0 / 2^2) = 2^0 + 2^-2 = 1,25

### A trabajar

¿Cuál es **el valor final** de la interpretación de la cadena ```1111``` en BSS(5,2)?