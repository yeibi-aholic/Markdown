# **MANUAL PYTHON**

1. **[Introducción a Python](#introduccion-a-python)**
2. **[Tipos de Datos Primitivos Simples](#tipos-de-datos-primitivos-simples)**
3. **[Entrada y Salida por Terminal](#entrada-y-salida-por-terminal)**
4. **[Condicionales](#condicionales)**
5. **[Bucles](#bucles)**
6. **[Listas](#listas)**
7. **[Tuplas](#tuplas)**
8. **[Diccionarios](#diccionarios)**
9. **[Funciones](#funciones)**
10. **[Programación funcional](#programacion-funcional)**
11. **[Comprensión de Colecciones](#comprension-de-colecciones)**
12. **[Ficheros](#ficheros)**
13. **[Excepciones](#excepciones)**
14. **[Programación orientada a Objetos](#programacion-orientada-a-objetos)**
15. **[Módulos](#modulos)**
16. **[Librería Datetime](#libreria-datetime)**
17. **[Librería Numpy](#libreria-numpy)**
18. **[Librería Pandas](#libreria-pandas)**
19. **[Librería Matplotlib](#libreria-matplotlib)**
20. **[Depuración de código](#depuracion-de-codigo)**
21. **[Referencias](#referencias)**

## **[<](#manual-python)**
## Introducción a Python
---
### ¿Qué es Python?
*[Python](https://www.python.org/)* es un lenguaje de programación de alto nivel multiparadigma que permite:

- Programación imperativa
- Programación funcional
- Programación orientada a objetos

Fue creado por Guido van Rossum en 1990 aunque actualmente es desarrollado y mantenido por la *Python Software Foundation*.

### Principales ventajas de Python
- Es de código abierto (certificado por la OSI).
- Es interpretable y compilable.
- Es fácil de aprender gracias a que su sintaxis es bastante legible para los humanos.
- Es un lenguaje maduro (29 años).
- Es fácilmente extensible e integrable en otros lenguajes (C, java).
- Esta mantenido por una gran comunidad de desarrolladores y hay multitud de recursos para su aprendizaje.

### Tipos de Ejecución
#### Interpretado en la consola de Python
Se ejecuta cada instrucción que introduce el usuario de manera interactiva.
~~~~ python
> python
>>> name = "Alf"
>>> print("Hola ", name)
Hola Alf
~~~~

#### Interpretado en fichero
Se leen y se ejecutan una a una todas las instrucciones del fichero.
~~~~ python
# Fichero hola.py
name = "Alf"
print("Hola ", name)
~~~~
~~~~ python
> python hola.py
Hola Alf
~~~~
También se puede hacer el fichero ejecutable indicando en la primera línea la ruta hasta el intérprete de Python.
~~~~ python
#!/usr/bin/python3
name = "Alf"
print("Hola", name)
~~~~
~~~~ python
> chmod +x hola.py
> ./hola.py
Hola Alf
~~~~

#### Compilado a bytecode
~~~~ python
# Fichero hola.py
name = "Alf"
print("Hola " + name)
~~~~
~~~~ python
> python -O -m py_compile hola.py
> python __pycache__/hola.cpython-37.pyc
Hola Alf
~~~~

#### Compilado a ejecutable del sistema
Hay distintos paquetes que permiten compilar a un ejecutable del sistema operativo usado, por ejemplo *pyinstaller*.
~~~~ python
> conda install pyinstaller
> pyinstaller hola.py
> ./dist/hola/hola
Hola Alf
~~~~

## **[<](#manual-python)**
## Tipos de Datos Primitivos Simples
---
### Tipos de datos primitivos simples
- **Números** (numbers): Secuencia de dígitos (pueden incluir el - para negativos y el . para decimales) que representan números.
> Ejemplo: 0, -1, 3.1415.
- **Cadenas** (strings): Secuencia de caracteres alfanuméricos que representan texto. Se escriben entre comillas simples o dobles.
> Ejemplo: ‘Hola’, “Adiós”.
- **Booleanos** (boolean): Contiene únicamente dos elementos *\<True>* y *\<False>* que representan los valores lógicos verdadero y falso respectivamente.

Estos datos son inmutables, es decir, su valor es constante y no puede cambiar.

### Tipos de datos primitivos compuestos (contenedores)
- **Listas** (lists): Colecciones de objetos que representan secuencias ordenadas de objetos de distintos tipos. Se representan con corchetes y los elementos se separan por comas.
> Ejemplo: [1, “dos”, [3, 4], True].
- **Tuplas** (tuples). Colecciones de objetos que representan secuencias ordenadas de objetos de distintos tipos. A diferencia de las listas son inmutables, es decir, que no cambian durante la ejecución. Se representan mediante paréntesis y los elementos se separan por comas.
> Ejemplo: (1, ‘dos’, 3)
- **Diccionarios** (dictionaries): Colecciones de objetos con una clave asociada. Se representan con llaves, los pares separados por comas y cada par contiene una clave y un objeto asociado separados por dos puntos.
> Ejemplo: {‘pi’:3.1416, ’e’:2.718}.

### Clase de un dato (*type()*)
La clase a la que pertenece un dato se obtiene con el comando *type()*.
~~~~ python
>>> type(1)
<class 'int'>
>>> type("Hola")
<class 'str'>
>>> type([1, "dos", [3, 4], True])
<class 'list'>
>>>type({'pi':3.1416, 'e':2.718})
<class 'dict'>
>>>type((1, 'dos', 3))
<class 'tuple'>
~~~~

### Números (clases *int* y *float*)
Secuencia de dígitos (pueden incluir el - para negativos y el . para decimales) que representan números. Pueden ser enteros (*int*) o reales (*float*).
~~~~ python
>>> type(1)
<class 'int'>
>>> type(-2)
<class 'int'>
>>> type(2.3)
<class 'float'>
~~~~

#### Operadores aritméticos
Operadores aritméticos: + (suma), - (resta), * (producto), / (cociente), // (cociente división entera), % (resto división entera), ** (potencia).
Orden de prioridad de evaluación:  
- Funciones predefinidas => Potencias => Productos y cocientes => Sumas y restas

Se puede saltar el orden de evaluación utilizando paréntesis ( ).
~~~~ python
>>> 2+3
5
>>> 5*-2
-10
>>> 5/2
2.5
>>> 5//2
2
>>> (2+3)**2
25
~~~~

#### Operadores lógicos con números
Devuelven un valor lógico o booleano.

- Operadores lógicos: == (igual que), > (mayor que), < (menor que), >= (mayor o igual que), \<= (menor o igual que), != (distinto de).
~~~~ python
>>> 3==3
True
>>> 3.1<=3
False
>>> -1!=1
True
~~~~

### Cadenas (clase *str*)
Secuencia de caracteres alfanuméricos que representan texto. Se escriben entre comillas sencillas ’ o dobles “.
~~~~ python
'Python'
"123"
'True'
# Cadena vacía
''
# Cadena con un espacio en blanco
' '
# Cambio de línea
'\n'
# Tabulador
'\t'
~~~~

#### Acceso a los elementos de una cadena
Cada carácter tiene asociado un índice que permite acceder a él.

|Cadena|P|y|t|h|o|n|
|:-:|:-:|
|Índice positivo|0|1|2|3|4|5|
|Índice negativo|-6|-5|-4|-3|-2|-1|

- *c[i]* devuelve el carácter de la cadena *c* con el índice *i*.

> ⚠️ El índice del primer carácter de la cadena es *0*.

También se pueden utilizar índices negativos para recorrer la cadena del final al principio.

> ⚠️ El índice del último carácter de la cadena es *-1*.

~~~~ python
>>> 'Python'[0]
'P'
>>> 'Python'[1]
'y'
>>> 'Python'[-1]
'n'
>>> 'Python'[6]
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
IndexError: string index out of range
~~~~

#### Subcadenas
- *c[i:j:k]* : Devuelve la subcadena de c desde el carácter con el índice *i* hasta el carácter anterior al índice *j*, tomando caracteres cada *k*.
~~~~ python
>>> 'Python'[1:4]
'yth'
>>> 'Python'[1:1]
''
>>> 'Python'[2:]
'thon'
>>> 'Python'[:-2]
'Pyth'
>>> 'Python'[:]
'Python'
>>> 'Python'[0:6:2]
'Pto'
~~~~

#### Operaciones con cadenas
- *c1 + c2* : Devuelve la cadena resultado de concatenar las cadenas c1 y c2.
- *c * n* : Devuelve la cadena resultado de concatenar n copias de la cadena c.
- *c1 in c2* : Devuelve *\<True>* si c1 es una cadena concenida en c2 y *\<False>* en caso contrario.
- *c1 not in c2* : Devuelve *\<True>* si c1 es una cadena no concenida en c2 y *\<False>* en caso contrario.
~~~~ python
>>> 'Me gusta ' + 'Python'
'Me gusta Python'
>>> 'Python' * 3
'PythonPythonPython'
>>> 'y' in 'Python'
True
>>> 'tho' in 'Python'
True
>>> 'to' not in 'Python'
True
~~~~

#### Operaciones de comparación de cadenas
- *c1 == c2* : Devuelve *\<True>* si la cadena *c1* es igual que la cadena *c2* y *\<False>* en caso contrario.
- *c1 > c2* : Devuelve *\<True>* si la cadena *c1* sucede a la cadena *c2* y *\<False>* en caso contrario.
- *c1 < c2* : Devuelve *\<True>* si la cadena *c1* antecede a la cadena *c2* y *\<False>* en caso contrario.
- *c1 >= c2* : Devuelve *\<True>* si la cadena *c1* sucede o es igual a la cadena *c2* y *\<False>* en caso contrario.
- *c1 <= c2* : Devuelve *\<True>* si la cadena *c1* antecede o es igual a la cadena *c2* y *\<False>* en caso contrario.
- *c1 != c2* : Devuelve *\<True>* si la cadena *c1* es distinta de la cadena *c2* y *\<False>* en caso contrario.

> ⚠️ Utilizan el orden establecido en el *[código ASCII](https://elcodigoascii.com.ar/)*.

~~~~ python
>>> 'Python' == 'python'
False
>>> 'Python' < 'python'
True
>>> 'a' > 'Z'
True
>>> 'A' >= 'Z'
False
>>> '' < 'Python'
True
~~~~

#### Funciones de cadenas
- *len(c)* : Devuelve el número de caracteres de la cadena *c*.
- *min(c)* : Devuelve el carácter menor de la cadena *c*.
- *max(c)* : Devuelve el carácter mayor de la cadena *c*.
- *c.upper()* : Devuelve la cadena con los mismos caracteres que la cadena *c* pero en mayúsculas.
- *c.lower()* : Devuelve la cadena con los mismos caracteres que la cadena *c* pero en minúsculas.
- *c.title()* : Devuelve la cadena con los mismos caracteres que la cadena *c* con el primer carácter en mayúsculas y el resto en minúsculas.
- *c.split(delimitador)* : Devuelve la lista formada por las subcadenas que resultan de partir la cadena *c* usando como delimitador la cadena delimitador. Si no se especifica el delimitador utiliza por defecto el espacio en blanco.

~~~~ python
>>> len('Python')
6
>>> min('Python')
'P'
>>> max('Python')
'y'
>>> 'Python'.upper()
'PYTHON'
>>> 'A,B,C'.split(',')
['A', 'B', 'C']
>>> 'I love Python'.split()
['I', 'love', 'Python']
~~~~

#### Cadenas formateadas (*format()*)
- *c.format(valores)* : Devuelve la cadena *c* tras sustituir los valores de la secuencia valores en los marcadores de posición de *c*. Los marcadores de posición se indican mediante llaves *{}* en la cadena *c*, y el reemplazo de los valores se puede realizar por posición, indicando en número de orden del valor dentro de las llaves, o por nombre, indicando el nombre del valor, siempre y cuando los valores se pasen con el formato nombre = valor.

~~~~ python
>>> 'Un {} vale {} {}'.format('€', 1.12, '$')
'Un € vale 1.12 $'
>>> 'Un {2} vale {1} {0}'.format('€', 1.12, '$')
'Un $ vale 1.12 €'
>>> 'Un {moneda1} vale {cambio} {moneda2}'.format(moneda1 = '€', cambio = 1.12, moneda2 = '$')
'Un € vale 1.12 $'
~~~~

Los marcadores de posición, a parte de indicar la posición de los valores de reemplazo, pueden indicar también el formato de estos. Para ello se utiliza la siguiente sintaxis:

- *\{:n}* : Alinea el valor a la izquierda rellenando con espacios por la derecha hasta los *n* caracteres.
- *\{:>n}* : Alinea el valor a la derecha rellenando con espacios por la izquierda hasta los *n* caracteres.
- *\{:^n}* : Alinea el valor en el centro rellenando con espacios por la izquierda y por la derecha hasta los *n* caracteres.
- *\{:nd}* : Formatea el valor como un número entero con *n* caracteres rellenando con espacios blancos por la izquierda.
- *\{:n.mf}* : Formatea el valor como un número real con un tamaño de *n* caracteres (incluído el separador de decimales) y *m* cifras decimales, rellenando con espacios blancos por la izquierda.

~~~~ python
>>> 'Hoy es {:^10}, mañana {:10} y pasado {:>10}'.format('lunes', 'martes', 'miércoles')
'Hoy es   lunes   , mañana martes     y pasado  miércoles'
>>> 'Cantidad {:5d}'.format(12)'
'Cantidad    12'
>>> 'Pi vale {:8.4f}'.format(3.141592)
'Pi vale   3.1416'
~~~~

### Datos lógicos o booleanos (clase *bool*)
Contiene únicamente dos elementos *\<True>* y *\<False>* que representan los valores lógicos verdadero y falso respectivamente.

False tiene asociado el valor *0* y *\<True>* tiene asociado el valor *1*.

#### Operaciones con valores lógicos
- Operadores lógicos: == (igual que), > (mayor), < (menor), >= (mayor o igual que), \<= (menor o igual que), != (distinto de).
- not b (negación) : Devuelve *\<True>* si el dato booleano *b* es *\<False>*, y *\<False>* en caso contrario.
- b1 and b2 : Devuelve *\<True>* si los datos booleanos *b1* y *b2* son *\<True>*, y *\<False>* en caso contrario.
- b1 or b2 : Devuelve *\<True>* si alguno de los datos booleanos *b1* o *b2* son *\<True>*, y *\<False>* en caso contrario.

#### Tabla de verdad
|x|y|not x|x and y|x or y|
|:-:|:-:|:-:|:-:|:-:|
|False|False|True|False|False|
|False|True|True|False|True|
|True|False|False|False|True|
|True|True|False|True|True|

~~~~ python
>>> not True
False
>>> False or True
True
>>> True and False
False
>>> True and True
True
~~~~

### Conversión de datos primitivos simples
Las siguientes funciones convierten un dato de un tipo en otro, siempre y cuando la conversión sea posible.

- int() convierte a entero.
> int('12') => 12  
> int(True) => 1  
> int('c') => Error
- float() convierte a real.
> float('3.14') => 3.14  
> float(True) => 1.0  
> float('III') => Error
- str() convierte a cadena.
> str(3.14) => '3.14'  
> str(True) => 'True'
- bool() convierte a lógico.
> bool('0') => False  
> bool('3.14') => True  
> bool('') => False  
> bool('Hola') => True

### Variables
Una variable es un identificador ligado a algún valor.

Reglas para nombrarlas:
- Comienzan siempre por una letra, seguida de otras letras o números.
- No se pueden utilizarse palabras reservadas del lenguaje.

A diferencia de otros lenguajes no tienen asociado un tipo y no es necesario declararlas antes de usarlas (tipado dinámico).

Para asignar un valor a una variable se utiliza el operador = y para borrar una variable se utiliza la instrucción *del*.
~~~~ python
lenguaje = 'Python'
x = 3.14
y = 3 + 2
# Asignación múltiple
a1, a2 = 1, 2
# Intercambio de valores
a, b = b, a
# Incremento (equivale a x = x + 2)
x += 2
# Decremento (equivale a x = x - 1)
x -= 1
# Valor no definido
x = None
del x
~~~~

## **[<](#manual-python)**
## Entrada y Salida por Terminal
---
### Entrada por terminal (*input()*)
Para asignar a una variable un valor introducido por el usuario en la consola se utiliza la instrucción

- *input(mensaje)* : Muestra la cadena *mensaje* por la terminal y devuelve una cadena con la entrada del usuario.

> ⚠️ El valor devuelto siempre es una cadena, incluso si el usuario introduce un dato numérico.

~~~~ python
>>> language = input('¿Cuál es tu lenguaje favorito? ')
¿Cuál es tu lenguaje favorito? Python
>>> language
'Python'
>>> age = input('¿Cuál es tu edad? ')
¿Cuál es tu edad? 20
>>> age
'20'
~~~~

#### Salida por terminal (*print()*)
Para mostrar un dato por la terminal se utiliza la instrucción
~~~~ python
print(dato1, ..., sep=' ', end='\n', file=sys.stdout)
~~~~
donde:
- *dato1, ...* son los datos a imprimir y pueden indicarse tantos como se quieran separados por comas.
- *sep* establece el separador entre los datos, que por defecto es un espacio en blanco *' '*.
- *end* indica la cadena final de la impresión, que por defecto es un cambio de línea *\n*.
- *file* indica la dirección del flujo de salida, que por defecto es la salida estándar *sys.stdout*.

~~~~ python
>>> print('Hola')
Hola
>>> name = 'Alf'
>>> print('Hola', name)
Hola Alf
>>> print('El valor de pi es', 3.1415)
El valor de pi es 3.1415
>>> print('Hola', name, sep='')
HolaAlf
>>> print('Hola', name, end='!\n')
Hola Alf!
~~~~


## **[<](#manual-python)**
## Condicionales
---
### Condicionales (*if*)
~~~~ python
if condición1:
    bloque código
elif condición2:
    bloque código
…
else :
    bloque código
~~~~

Evalúa la expresión lógica *condición1* y ejecuta el primer bloque de código si es *\<True>*; si no, evalúa la siguientes condiciones hasta llegar a la primera que es *\<True>* y ejecuta el bloque de código asociado. Si ninguna condición es *\<True>* ejecuta el bloque de código después de *else*:.

Pueden aparecer varios bloques *elif* pero solo uno else al final.

> ⚠️ Los bloques de código deben estar indentados por 4 espacios.

La instrucción condicional permite evaluar el estado del programa y tomar decisiones sobre qué código ejecutar en función del mismo.

~~~~ python
>>> edad = 14
>>> if edad <= 18 : 
...     print('Menor')
... elif edad > 65:
...     print('Jubilado')
... else:
...     print('Activo')
...
Menor
>>> age = 20
>>> if edad <= 18 : 
...     print('Menor')
... elif edad > 65:
...     print('Jubilado')
... else:
...     print('Activo')
...
Activo
~~~~


## **[<](#manual-python)**
## Bucles
---
### Bucles condicionales (*while*)
~~~~ python
while condición:
    bloque código
~~~~

Repite la ejecución del bloque de código mientras la expresión lógica *condición* sea cierta.

Se puede interrumpir en cualquier momento la ejecución del bloque de código con la instrucción *break*.

> ⚠️ El bloque de código debe estar indentado por 4 espacios.

~~~~ python
>>> # Pregunta al usuario por un número hasta que introduce 0.
>>> num = None
>>> while num != 0:
...     num = int(input('Introduce un número: '))
... 
Introduce un número: 2
Introduce un número: 1
Introduce un número: 0
>>> 
~~~~

Alternativa:
~~~~ python
>>> # Pregunta al usuario por un número hasta que introduce 0.
>>> while True:
...     num = int(input('Introduce un número: '))
...     if num == 0:
...         break
...
Introduce un número: 2
Introduce un número: 1
Introduce un número: 0
>>>
~~~~

### Bucles iterativos (*for*)
~~~~ python
for i in secuencia:
    bloque código
~~~~

Repite la ejecución del bloque de código para cada elemento de la secuencia *secuencia*, asignado dicho elemento a *i* en cada repetición.

Se puede interrumpir en cualquier momento la ejecución del bloque de código con la instrucción *break* o saltar la ejecución para un determinado elemento de la secuencia con la instrucción *continue*.

> ⚠️ El bloque de código debe estar indentado por 4 espacios.

Se utiliza fundamentalmente para recorrer colecciones de objetos como cadenas, listas, tuplas o diccionarios.

A menudo se usan con la instrucción *range*:

- *range(fin)* : Genera una secuencia de números enteros desde *0* hasta *fin-1*.
- *range(inicio, fin, salto)* : Genera una secuencia de números enteros desde *inicio* hasta *fin-1* con un incremento de *salto*.

~~~~ python
>>> palabra = 'Python'
>>> for letra in palabra:
...     print(letra)
... 
P
y
t
h
o
n
~~~~
~~~~ python
>>> for i in range(1, 10, 2):
...     print(i, end=", ")
...
1, 3, 5, 7, 9, >>>
~~~~


## **[<](#manual-python)**
## Listas
---
### Listas
Una *lista* es una secuencias ordenadas de objetos de distintos tipos.

Se construyen poniendo los elementos entre corchetes *[ ]* separados por comas.

Se caracterizan por:
- Tienen orden.
- Pueden contener elementos de distintos tipos.
- Son mutables, es decir, pueden alterarse durante la ejecución de un programa.

~~~~ python
# Lista vacía
>>> type([])
<class 'list'>
# Lista con elementos de distintos tipos
>>> [1, "dos", True]
# Listas anidadas
>>> [1, [2, 3], 4]
~~~~

#### Creación de listas mediante la función *list()*
Otra forma de crear listas es mediante la función *list()*.

- *list(c)* : Crea una lista con los elementos de la secuencia o colección *c*.

Se pueden indicar los elementos separados por comas, mediante una cadena, o mediante una colección de elementos iterable.

~~~~ python
>>> list()
[]
>>> list(1, 2, 3)
[1, 2, 3]
>>> list("Python")
['P', 'y', 't', 'h', 'o', 'n']
~~~~

#### Acceso a los elementos de una lista
Se utilizan los mismos operadores de acceso que para cadenas de caracteres.

- *l[i]* : Devuelve el elemento de la lista *l* con el índice *i*.

> ⚠️ El índice del primer elemento de la lista es *0*.

~~~~ python
>>> a = ['P', 'y', 't', 'h', 'o', 'n']
>>> a[0]
'P'
>>> a[5]
'n'
>>> a[6]
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
IndexError: list index out of range
>>> a[-1]
'n'
~~~~

#### Sublistas
- *l[i:j:k]* : Devuelve la sublista desde el elemento de *l* con el índice *i* hasta el elemento anterior al índice *j*, tomando elementos cada *k*.
~~~~ python
>>> a = ['P', 'y', 't', 'h', 'o', 'n']
>>> a[1:4]
['y', 't', 'h']
>>> a[1:1]
[]
>>> a[:-3]
['P', 'y', 't']
>>> a[:]
['P', 'y', 't', 'h', 'o', 'n']
>>> a[0:6:2]
['P', 't', 'o']
~~~~

#### Operaciones que no modifican una lista
- *len(l)* : Devuelve el número de elementos de la lista *l*.
- *min(l)* : Devuelve el mínimo elemento de la lista *l* siempre que los datos sean comparables.
- *max(l)* : Devuelve el máximo elemento de la lista *l* siempre que los datos sean comparables.
- *sum(l)* : Devuelve la suma de los elementos de la lista *l*, siempre que los datos se puedan sumar.
- *dato in l* : Devuelve *\<True>* si el *dato* dato pertenece a la lista *l* y *\<False>* en caso contrario.
- *l.index(dato)* : Devuelve la posición que ocupa en la lista *l* el primer elemento con valor *dato*.
- *l.count(dato)* : Devuelve el número de veces que el valor *dato* está contenido en la lista *l*.
- *all(l)* : Devuelve *\<True>* si todos los elementos de la lista *l* son *\<True>* y *\<False>* en caso contrario.
- *any(l)* : Devuelve *\<True>* si algún elemento de la lista *l* es *\<True>* y *\<False>* en caso contrario.

~~~~ python
>>> a = [1, 2, 2, 3]
>>> len(a)
4
>>> min(a)
1
>>> max(a)
3
>>> sum(a)
8
>>> 3 in a
True
>>> a.index(2)
1
>>> a.count(2)
2
>>> all(a)
True
>>> any([0, False, 3<2])
False
~~~~

#### Operaciones que modifican una lista
- *l1 + l2* : Crea una nueva lista concatenan los elementos de la listas *l1* y *l2*.
- *l.append(dato)* : Añade dato al final de la lista *l*.
- *l.extend(sequencia)* : Añade los datos de sequencia al final de la lista *l*.
- *l.insert(índice, dato)* : Inserta *dato* en la posición *índice* de la lista *l* y desplaza los elementos una posición a partir de la posición *índice*.
- *l.remove(dato)* : Elimina el primer elemento con valor *dato* en la lista *l* y desplaza los que están por detrás de él una posición hacia delante.
- *l.pop([índice])* : Devuelve el dato en la posición *índice* y lo elimina de la lista *l*, desplazando los elementos por detrás de él una posición hacia delante. Por defecto elimina el último valor de la lista.
- *l.sort()* : Ordena los elementos de la lista *l* de acuerdo al orden predefinido, siempre que los elementos sean comparables.
- *l.reverse()* : invierte el orden de los elementos de la lista *l*.

~~~~ python
>>> a = [1, 3]
>>> b = [2, 4, 6]
>>> a.append(5)
>>> a
[1, 3, 5]
>>> a.remove(3)
>>> a
[1, 5]
>>> a.insert(1, 3)
>>> a
[1, 3, 5]
>>> b.pop()
6
>>> c = a + b
>>> c
[1, 3, 5, 2, 4]
>>> c.sort()
>>> c
[1, 2, 3, 4, 5]
>>> c.reverse()
>>> c
[5, 4, 3, 2, 1]
~~~~

#### Copia de listas
Existen dos formas de copiar listas:
- **Copia por referencia** *l1 = l2* : Asocia la la variable *l1* la misma lista que tiene asociada la variable *l2*; es decir, ambas variables apuntan a la misma dirección de memoria. Cualquier cambio que hagamos a través de *l1* o *l2* afectará a la misma lista.
- **Copia por valor** *l1 = list(l2)* : Crea una copia de la lista asociada a *l2* en una dirección de memoria diferente y se la asocia a *l1*. Las variables apuntan a direcciones de memoria diferentes que contienen los mismos datos. Cualquier cambio que hagamos a través de *l1* no afectará a la lista de *l2* y viceversa.
~~~~ python
>>> a = [1, 2, 3]
>>> # copia por referencia
>>> b = a
>>> b
[1, 2, 3]
>>> b.remove(2)
>>> b
[1, 3]
>>> a
[1, 3]
~~~~
~~~~ python
>>> a = [1, 2, 3]
>>> # copia por referencia
>>> b = list(a)
>>> b
[1, 2, 3]
>>> b.remove(2)
>>> b
[1, 3]
>>> a
[1, 2, 3]
~~~~


## **[<](#manual-python)**
## Tuplas
---
### Tuplas
Una tupla es una secuencias ordenadas de objetos de distintos tipos.

Se construyen poniendo los elementos entre corchetes *( )* separados por comas.

Se caracterizan por:
- Tienen orden.
- Pueden contener elementos de distintos tipos.
- Son inmutables, es decir, no pueden alterarse durante la ejecución de un programa.

Se usan habitualmente para representar colecciones de datos una determinada estructura semántica, como por ejemplo un vector o una matriz.

~~~~ python
# Tupla vacía
type(())
<class 'tuple'>
# Tupla con elementos de distintos tipos
(1, "dos", True)
# Vector
(1, 2, 3)
# Matriz
((1, 2, 3), (4, 5, 6))
~~~~

#### Creación de tuplas mediante la función *tuple()*
Otra forma de crear tuplas es mediante la función *tuple()*.

- *tuple(c)* : Crea una tupla con los elementos de la secuencia o colección *c*.

Se pueden indicar los elementos separados por comas, mediante una cadena, o mediante una colección de elementos iterable.

~~~~ python
>>> tuple()
()
>>> tuple(1, 2, 3)
(1, 2, 3)
>>> tuple("Python")
('P', 'y', 't', 'h', 'o', 'n')
>>> tuple([1, 2, 3])
(1, 2, 3)
~~~~

#### Operaciones con tuplas
El acceso a los elementos de una tupla se realiza del mismo modo que en las listas. También se pueden obtener subtuplas de la misma manera que las sublistas.

Las operaciones de listas que no modifican la lista también son aplicables a las tuplas.

~~~~ python
>>> a = (1, 2, 3)
>>> a[1]
2
>>> len(a)
3
>>> a.index(3)
2
>>> 0 in a
False
>>> b = ((1, 2, 3), (4, 5, 6))
>>> b[1]
(4, 5, 6)
>>> b[1][2]
6
~~~~


## **[<](#manual-python)**
## Diccionarios
---
### Diccionarios
Un diccionario es una colección de pares formados por una clave y un valor asociado a la clave.

Se construyen poniendo los pares entre llaves *{ }* separados por comas, y separando la clave del valor con dos puntos *:*.

Se caracterizan por:
- No tienen orden.
- Pueden contener elementos de distintos tipos.
- Son mutables, es decir, pueden alterarse durante la ejecución de un programa.
- Las claves son únicas, es decir, no pueden repetirse en un mismo diccionario, y pueden ser de cualquier tipo de datos inmutable.

~~~~ python
# Diccionario vacío
type({})
<class 'dict'>
# Diccionario con elementos de distintos tipos
{'nombre':'Alfredo', 'despacho': 218, 'email':'asalber@ceu.es'}
# Diccionarios anidados
{'nombre_completo':{'nombre': 'Alfredo', 'Apellidos': 'Sánchez Alberca'}}
~~~~

#### Acceso a los elementos de un diccionario
- *d[clave]* devuelve el valor del diccionario *d* asociado a la clave *clave*. Si en el diccionario no existe esa clave devuelve un error.
- *d.get(clave, valor)* devuelve el valor del diccionario *d* asociado a la clave *clave*. Si en el diccionario no existe esa clave devuelve valor, y si no se especifica un valor por defecto devuelve *None*.

~~~~ python
>>> a = {'nombre':'Alfredo', 'despacho': 218, 'email':'asalber@ceu.es'}
>>> a['nombre']
'Alfredo'
>>> a['despacho'] = 210
>>> a
{'nombre':'Alfredo', 'despacho': 210, 'email':'asalber@ceu.es'}
>>> a.get('email')
'asalber@ceu.es'
>>> a.get('universidad', 'CEU')
'CEU'
~~~~

#### Operaciones que no modifican un diccionario
- *len(d)* : Devuelve el número de elementos del diccionario *d*.
- *min(d)* : Devuelve la mínima clave del diccionario *d* siempre que las claves sean comparables.
- *max(d)* : Devuelve la máxima clave del diccionario *d* siempre que las claves sean comparables.
- *sum(d)* : Devuelve la suma de las claves del diccionario *d*, siempre que las claves se puedan sumar.
- *clave in d* : Devuelve *\<True>* si la clave *clave* pertenece al diccionario *d* y *\<False>* en caso contrario.
- *d.keys()* : Devuelve un iterador sobre las claves de un diccionario.
- *d.values()* : Devuelve un iterador sobre los valores de un diccionario.
- *d.items()* : Devuelve un iterador sobre los pares clave-valor de un diccionario.

~~~~ python
>>> a = {'nombre':'Alfredo', 'despacho': 218, 'email':'asalber@ceu.es'}
>>> len(a)
3
>>> min(a)
'despacho'
>>> 'email' in a
True
>>> a.keys()
dict_keys(['nombre', 'despacho', 'email'])
>>> a.values()
dict_values(['Alfredo', 218, 'asalber@ceu.es'])
>>> a.items()
dict_items([('nombre', 'Alfredo'), ('despacho', 218), ('email', 'asalber@ceu.es')])
~~~~

#### Operaciones que modifican un diccionario
- *d[clave] = valor* : Añade al diccionario *d* el par formado por la clave *clave* y el valor *valor*.
- *d.update(d2)* :: Añade los pares del diccionario *d2* al diccionario *d*.
- *d.pop(clave, alternativo)* : Devuelve del valor asociado a la clave *clave* del diccionario *d* y lo elimina del diccionario. Si la clave no está devuelve el valor *alternativo*.
- *d.popitem()* : Devuelve la tupla formada por la clave y el valor del último par añadido al diccionario *d* y lo elimina del diccionario.
- *del d[clave]* : Elimina del diccionario *d* el par con la clave *clave*.
- *d.clear()* : Elimina todos los pares del diccionario *d* de manera que se queda vacío.

~~~~ python
>>> a = {'nombre':'Alfredo', 'despacho': 218, 'email':'asalber@ceu.es'}
>>> a['universidad'] = 'CEU'
>>> a
{'nombre': 'Alfredo', 'despacho': 218, 'email': 'asalber@ceu.es', 'universidad': 'CEU'}
>>> a.pop('despacho')
218
>>> a
{'nombre': 'Alfredo', 'email': 'asalber@ceu.es', 'universidad': 'CEU'}
>>> a.popitem()
('universidad', 'CEU')
>>> a
{'nombre': 'Alfredo', 'email': 'asalber@ceu.es'}
>>> del a['email']
>>> a
{'nombre': 'Alfredo'}
>>> a.clear()
>>> a
{}
~~~~

#### Copia de diccionarios
Existen dos formas de copiar diccionarios:
- **Copia por referencia** *d1 = d2* : Asocia la la variable *d1* el mismo diccionario que tiene asociado la variable *d2*, es decir, ambas variables apuntan a la misma dirección de memoria. Cualquier cambio que hagamos a través de *l1* o *l2* afectará al mismo diccionario.
- **Copia por valor** *d1 = list(d2)* : Crea una copia del diccionario asociado a *d2* en una dirección de memoria diferente y se la asocia a *d1*. Las variables apuntan a direcciones de memoria diferentes que contienen los mismos datos. Cualquier cambio que hagamos a través de *l1* no afectará al diccionario de *l2* y viceversa.

~~~~ python
>>> a = {1:'A', 2:'B', 3:'C'}
>>> # copia por referencia
>>> b = a
>>> b
{1:'A', 2:'B', 3:'C'}
>>> b.pop(2)
>>> b
{1:'A', 3:'C'}
>>> a
{1:'A', 3:'C'}
~~~~
~~~~ python
>>> a = {1:'A', 2:'B', 3:'C'}
>>> # copia por referencia
>>> b = dict(a)
>>> b
{1:'A', 2:'B', 3:'C'}
>>> b.pop(2)
>>> b
{1:'A', 3:'C'}
>>> a
{1:'A', 2:'B', 3:'C'}
~~~~


## **[<](#manual-python)**
## Funciones
---
### Funciones (def)
Una función es un bloque de código que tiene asociado un nombre, de manera que cada vez que se quiera ejecutar el bloque de código basta con invocar el nombre de la función.

Para declarar una función se utiliza la siguiente sintaxis:

~~~~ python
def <nombre-funcion> (<parámetros>):
     bloque código
     return <objeto>
~~~~

~~~~ python
>>> def bienvenida():
...     print('¡Bienvenido a Python!')
...     return
...
>>> type(bienvenida)
<class 'function'>
>>> bienvenida()
¡Bienvenido a Python!
~~~~

#### Parámetros y argumentos de una función
Una función puede recibir valores cuando se invoca a través de unas variables conocidas como *parámetros* que se definen entre paréntesis en la declaración de la función. En el cuerpo de la función se pueden usar estos parámetros como si fuesen variables.

Los valores que se pasan a la función en una llamada o invocación concreta de ella se conocen como *argumentos* y se asocian a los parámetros de la declaración de la función.

~~~~ python
>>> def bienvenida(nombre):
...     print('¡Bienvenido a Python', nombre + '!')
...     return
...
>>> bienvenida('Alf')
¡Bienvenido a Python Alf!
~~~~

#### Paso de argumentos a una función
Los argumentos se pueden pasar de dos formas:

- **Argumentos posicionales** : Se asocian a los parámetros de la función en el mismo orden que aparecen en la definición de la función.
- **Argumentos nominales** : Se indica explícitamente el nombre del parámetro al que se asocia un argumento de la forma *parametro = argumento*.

~~~~ python
>>> def bienvenida(nombre, apellido):
...     print('¡Bienvenido a Python', nombre, apellido + '!')
...     return
...
>>> bienvenida('Alfredo', 'Sánchez')
¡Bienvenido a Python Alfredo Sánchez!
>>> bienvenida(apellido = 'Sánchez', nombre = 'Alfredo')
¡Bienvenido a Python Alfredo Sánchez!
~~~~

#### Retorno de una función
Una función puede devolver un objeto de cualquier tipo tras su invocación. Para ello el objeto a devolver debe escribirse detrás de la palabra reservada *return*. Si no se indica ningún objeto, la función no devolverá nada.
~~~~ python
>>> def area_triangulo(base, altura):
...     return base * altura / 2
...
>>> area_triangulo(2, 3)
3
>>> area_triangulo(4, 5)
10
~~~~

Una función puede devolver más de un objeto separándolos por comas tras la palabra reservada *return*. En tal caso, la función agrupará los objetos en una tupla y devolverá la tupla.

### Argumentos por defecto
En la definición de una función se puede asignar a cada parámetro un argumento por defecto, de manera que si se invoca la función sin proporcionar ningún argumento para ese parámetro, se utiliza el argumento por defecto.

~~~~ python
>>> def bienvenida(nombre, lenguaje = 'Python'):
...     print('¡Bienvenido a', lenguaje, nombre + '!')
...     return
...
>>> bienvenida('Alf')
¡Bienvenido a Python Alf!
>>> bienvenida('Alf', 'Java')
¡Bienvenido a Java Alf!
~~~~

> ⚠️ Los parámetros con un argumento por defecto deben indicarse después de los parámetros sin argumentos por defectos. De lo contrario se produce un error.

### Pasar un número indeterminado de argumentos
Por último, es posible pasar un número variable de argumentos a un parámetro. Esto se puede hacer de dos formas:

- **parametro* : Se antepone un asterisco al nombre del parámetro y en la invocación de la función se pasa el número variable de argumentos separados por comas. Los argumentos se guardan en una lista que se asocia al parámetro.
~~~~ python
>>> def menu(*platos):
...     print('Hoy tenemos: ', end='')
...     for plato in platos:
...         print(plato, end=', ')
...     return
...
>>> menu('pasta', 'pizza', 'ensalada')
Hoy tenemos: pasta, pizza, ensalada,
~~~~

- ***parametro* : Se anteponen dos asteriscos al nombre del parámetro y en la invocación de la función se pasa el número variable de argumentos por pares *nombre = valor*, separados por comas. Los argumentos se guardan en un diccionario que se asocia al parámetro.
~~~~ python
>>> def contacto(**info):
...     print('Datos del contacto')
...     for clave, valor in info.items():
...         print(clave, ":", valor)
...     return
...
>>> contacto(Nombre = "Alf", Email = "asalber@ceu.es")
Datos del contacto
Nombre : Alf
Email : asalber@ceu.es
>>> contacto(Nombre = "Alf", Email = "asalber@ceu.es", Dirección = "Madrid")
Datos del contacto
Nombre : Alf
Email : asalber@ceu.es
Dirección : Madrid
~~~~

### Ámbito de los parámetros y variables de una función
Los parámetros y las variables declaradas dentro de una función son de **ámbito local**, mientras que las definidas fuera de ella son de ámbito **ámbito global**.

Tanto los parámetros como las variables del ámbito local de una función sólo están accesibles durante la ejecución de la función, es decir, cuando termina la ejecución de la función estas variables desaparecen y no son accesibles desde fuera de la función.

~~~~ python
>>> def bienvenida(nombre):
...     lenguaje = 'Python'
...     print('¡Bienvenido a ', lenguaje, nombre + '!')
...     return
...
>>> bienvenida('Alf')
¡Bienvenido a Python Alf!
>>> lenguaje
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
NameError: name 'lenguaje' is not defined
~~~~

Si en el ámbito local de una función existe una variable que también existe en el ámbito global, durante la ejecución de la función la variable global queda eclipsada por la variable local y no es accesible hasta que finaliza la ejecución de la función.

~~~~ python
>>> lenguaje = 'Java'
>>> def bienvenida():
...     lenguaje = 'Python'
...     print('¡Bienvenido a', lenguaje + '!')
...     return
...
>>> bienvenida()
¡Bienvenido a Python!
>>> print(lenguaje)
Java
~~~~

### Paso de argumentos por asignación
En Python los argumentos se pasan a una función por asignación, es decir, se asignan a los parámetros de la función como si fuesen variables locales. De este modo, cuando los argumentos son objetos mutables (listas, diccionarios, etc.) se pasa al parámetro una referencia al objeto, de manera que cualquier cambio que se haga dentro de la función mediante el parámetro asociado afectará al objeto original.

~~~~ python
>>> primer_curso = ['Matemáticas', 'Física']
>>> def añade_asignatura(curso, asignatura):
...     curso.append(asignatura)
...     return
...
>>> añade_asignatura(primer_curso, 'Química')
>>> print(primer_curso)
['Matemáticas', 'Física', 'Química']
~~~~

### Las funciones son objetos
En Python las funciones son objetos como el resto de tipos de datos, de manera que es posible asignar una función a una variable y luego utilizar la variable para hacer la llamada a la función.

~~~~ python
>>> def saludo(nombre):
...     print("Hola", nombre)
...     return
... 
>>> bienvenida = saludo
>>> bienvenida("Alf")
Hola Alf
~~~~

Esto permite, por tanto, pasar funciones como argumentos en la llamada a una función y que una función pueda devolver otras funciones.

~~~~ python
>>> def impuesto(porcentaje):
...     def aplicar(base):
...             return base * porcentaje / 100
...     return aplicar
... 
>>> iva = impuesto(21)
>>> iva(1000)
210.0
~~~~

### Funciones recursivas
Una función recursiva es una función que en su cuerpo contiene una llama a si misma.

La recursión es una práctica común en la mayoría de los lenguajes de programación ya que permite resolver las tareas recursivas de manera más natural.

Para garantizar el final de una función recursiva, las sucesivas llamadas tienen que reducir el grado de complejidad del problema, hasta que este pueda resolverse directamente sin necesidad de volver a llamar a la función.

~~~~ python
>>> def factorial(n):
...     if n == 0:
...         return 1
...     else:
...         return n * factorial(n-1)
...
>>> f(5)
120
~~~~

#### Funciones recursivas múltiples
Una función recursiva puede invocarse a si misma tantas veces como quiera en su cuerpo.
~~~~ python
>>> def fibonacci(n):
...     if n <= 1:
...         return n
...     else:
...         return fibonacci(n - 1) + fibonacci(n - 2)
...
>>> fibonacci(6)
8
~~~~

#### Los riesgos de la recursión
Aunque la recursión permite resolver las tareas recursivas de forma más natural, hay que tener cuidado con ella porque suele consumir bastante memoria, ya que cada llamada a la función crea un nuevo ámbito local con las variables y los parámetros de la función.

En muchos casos es más eficiente resolver la tarea recursiva de forma iterativa usando bucles.
~~~~ python
>>> def fibonacci(n):
...     a, b = 0, 1
...     for i in range(n):
...         a, b = b, a + b
...     return a
...
>>> fibonacci(6)
8
~~~~

### Documentación de funciones
Una práctica muy recomendable cuando se define una función es describir lo que la función hace en un comentario.

En Python esto se hace con un **docstring** que es un tipo de comentario especial se hace en la línea siguiente al encabezado de la función entre tres comillas simples *'''* o dobles *"""*.

Después se puede acceder a la documentación de la función con la función *help(<nombre-función>)*.

~~~~ python
>>> def area_triangulo(base, altura):
... """
... Función que calcula el área de un triángulo.
...
... Parámetros:
...     - base: Un número real con la base del triángulo.
...     - altura: Un número real con la altura del triángulo.
... Salida:
...     Un número real con el área del triángulo de base y altura especificadas.
... """
...     return base * altura / 2
...
>>> help(area_triangulo)
area_triangulo(base, altura)
    Función que calcula el área de un triángulo.

    Parámetros:
        - base: Un número real con la base del triángulo.
        - altura: Un número real con la altura del triángulo.
    Salida:
        Un número real con el área del triángulo de base y altura especificadas.
~~~~





## **[<](#manual-python)**
## Programación funcional
---
## **[<](#manual-python)**
## Comprensión de Colecciones
---
## **[<](#manual-python)**
## Ficheros
---
## **[<](#manual-python)**
## Excepciones
---
## **[<](#manual-python)**
## Programación orientada a Objetos
---
## **[<](#manual-python)**
## Módulos
---
## **[<](#manual-python)**
## Librería Datetime
---
## **[<](#manual-python)**
## Librería Numpy
---
## **[<](#manual-python)**
## Librería Pandas
---
## **[<](#manual-python)**
## Librería Matplotlib
---
## **[<](#manual-python)**
## Depuración de código
---
## **[<](#manual-python)**
## Referencias
---