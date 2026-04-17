# Operador ADDI
###¿Que hace?
Este operador toma un registro de 16 bits y le suma una constante de 8 bits (ambos en complemento a 2). Siendo que tiene en cuenta el signo de ambos numeros, cuenta tambien con una funcion que detecta si hubo o no un overflow.
###¿Como funciona?
El registro y la constante se conectan a un sumador de 16 bits (usando un splitter en el caso de la constante). El sumador se conecta a una constante de un unico bit en 0 que le indica que ignore el acarreo.
Para implementar la funcion de overflow se utilizan una compuerta logica XOR, una compuerta logica XNOR y una compuerta logica AND. Tanto el XOR como el XNOR tienen una entrada conectada al registro src, tambien estan conectados al resultado y a la constante respectivamente. La salida de ambas compuertas se conectan a un AND. La salida de dicho AND debera ser 1 si se insertan un registro y una constante de igual signo pero se obtiene un resultado se digno contrario. En el caso del ejemplo no ocurre un overflow. 
