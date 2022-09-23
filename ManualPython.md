#### Operadores bit a bit
Realizan operaciones en los operandos bit a bit (en binario)

|Operador|Equivalencia|
|:-:|:-|
|\||**OR** bit a bit|
|^|**XOR** bit a bit|
|&|**AND** bit a bit|
|~|**NOT** - Obtiene los bits invertidos|
|>>n|Desplaza n bits a la derecha|
|<<n|Desplaza n bits a la izquierda|

~~~~ python
>>> x = 10  # 01010
>>> y = 7   # 00111
>>> x | y   # 01010 OR 00111 --> 01111
15
>>> x ^ y   # 01010 XOR 00111 --> 01101
13
>>> x & y   # 01010 AND 00111 --> 00010
2
>>> y<<1    # 00111 --> 01110
14
>>> y>>1    # 00111 --> 00011
1
>>> ~x      # 01010 --> -(01010 + 00001) = -01011
-11
~~~~
