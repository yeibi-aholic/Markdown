# **GU�A MARKDOWN**
## �NDICE
1. **[ENCABEZADOS](#encabezados)**
2. **[P�RRAFOS](#p�rrafos)**
3. **[L�NEA HORIZONTAL](#l�nea-horizontal)**
4. **[�NFASIS DE TEXTO](#�nfasis-de-texto)**  
   - **[Cursiva](#cursiva)**  
   - **[Negrita](#negrita)**  
   - **[Negrita y Cursiva](#negrita-y-cursiva)** 
   - **[Tachado](#tachado)**
   - **[Sub�ndice](#sub�ndice)**
   - **[Super�ndice](#super�ndice)** 
   - **[Color](#color)**  
   - **[Tipograf�a](#tipograf�a)**
5. **[LISTAS](#listas)**  
   - **[Ordenadas](#ordenadas)**  
   - **[No ordenadas](#no-ordenadas)**  
   - **[Sublistas](#sublistas)**   
6. **[TABLAS](#tablas)**
7. **[CITAS](#citas)**
8. **[C�DIGO](#c�digo)**
9. **[LINKS](#links)**  
    - **[Enlaces web](#enlaces-web)**
    - **[Llamada de encabezados](#llamada-de-encabezados)**
    - **[Referencias](#referencias)**   
    - **[Documentos](#documentos)**  
    - **[Im�genes](#im�genes)**        
10. **[INHABILITACI�N DE COMANDOS MARKDOWN](#inhabilitaci�n-de-comandos-markdown)**  

## ENCABEZADOS
---
Para crear un encabezado tan solo hace falta poner al principio de un p�rrafo el s�mbolo *#* y un espacio. Dependiento del n�mero de s�mbolos que se empleen corresponder� a un *nivel de t�tulo*.

# T�tulo 1
~~~~
# T�tulo 1
~~~~

## T�tulo 2
~~~~
## T�tulo 2
~~~~

### T�tulo 3
~~~~
### T�tulo 3
~~~~

#### T�tulo 4
~~~~
#### T�tulo 4
~~~~

##### T�tulo 5
~~~~
##### T�tulo 5
~~~~

###### T�tulo 6
~~~~
###### T�tulo 6
~~~~

### Alternativas para # T�tulo 1 y ## T�tulo 2  
Para estos dos casos existe la posibilidad de escribirlos con *=* y *-* estando por debajo del texto.

T�tulo 1
========
~~~~
T�tulo 1  
========
~~~~

T�tulo 2
--------
~~~~
T�tulo 2  
--------
~~~~

## P�RRAFOS
---
Para separar dos p�rrafos se deben poner dos espacios al final del primero o dejar una l�nea en blanco entre los dos.

- **Dos espacios:**

P�rrafo 1  
P�rrafo 2

- **L�nea en blanco:** 

P�rrafo 1

P�rrafo 2

## L�NEA HORIZONTAL
---
Para crear una *l�nea horizontal* solo es necesario poner en una l�nea aparte 3 asteriscos (***), 3 guiones (---) o 3 barras bajas (___). La l�nea se ver� igual en los tres casos.

~~~~
---  
***  
___
~~~~  

## �NFASIS DE TEXTO
---
#### Cursiva
Poner entre aster�scos (\*[  ]*) o barras bajas (\_[  ]_) el texto deseado sin espacios ni al principio ni al final: *Cursiva*.  

#### Negrita
Poner entre dos aster�scos (\*\*[  ]**) o dos barras bajas (\_\_[  ]__) el texto deseado sin espacios ni al principio ni al final: **Negrita**

#### Negrita y Cursiva
Poner entre tres aster�scos (\*\*\*[  ]***) o tres barras bajas (\_\_\_[  ]___) el texto deseado sin espacios ni al principio ni al final: ***Negrita y Cursiva***

#### Tachado
Poner entre dos virgulillas (\~~[  ]~~) el texto deseado sin espacios ni al principio ni al final: ~~Tachado~~

#### Sub�ndice
Poner entre virgulillas (\~[  ]~) el texto deseado sin espacios ni al principio ni al final: ~sub�ndice~

#### Super�ndice
Poner entre acentos circunflejos (\^[  ]^) el texto deseado sin espacios ni al principio ni al final: ^super�ndice^

#### Color
Escribir **\<span style = "color: *'color deseado (en ingl�s)'*">** y **\</span>** entre el texto al que se quiere aplicar el color: 
<span style = "color: red"> rojo </span> / <span style = "color: blue"> azul </span> / <span style = "color: green"> verde </span> / <span style = "color: orange"> naranja </span> / <span style = "color: purple"> morado </span>

#### Tipograf�a
Escribir **\<span style = "font-family: *'nombre de la tipograf�a'*">** y **\</span>** entre el texto al que se le quiere cambiar la tipograf�a: 
<span style = "font-family: Papyrus"> Papyrus </span> / <span style = "font-family: Georgia"> Georgia </span> / <span style = "font-family: Arial Black"> Arial Black </span> / <span style = "font-family: Calibri"> Calibri </span> / <span style = "font-family: Script"> Script </span>

## LISTAS
---
Hay dos formatos de listas: con guiones (no ordenadas) o num�ricas (ordenadas).

- #### Ordenadas
Se trata de p�rrafos seguidos donde al comienzo se encuentra un n�mero y seguido un punto.

~~~~
1. Primero  
2. Segundo  
3. Tercero
~~~~ 

1. Primero  
2. Segundo  
3. Tercero  

> No hace falta que los numeros sigan un orden. La lista seguir� el orden del primer n�mero escrito (no hace falta que sea "1.") y en la siguienta l�nea, independientemente que n�mero est� escrito en la misma, continuar� al n�mero anterior.

- #### No ordenadas
Hay varios guiones validos para que *Markdown* los interprete como lista: -, *, +.

~~~~
- A  
- a  
+ B  
+ b  
* C  
* c
~~~~  

- A  
- a  
+ B  
+ b  
* C  
* c

> Cuando se ponen dos simbolos de listado diferentes en dos l�neas seguidas, *Markdown* los separar� un poco m�s que si fuesen ambos del mismo s�mbolo.

- #### Sublistas
Se tratar�a de tabular al mismo nivel los elementos que se deseen que pertenezcan a un elemento de la lista concreto.

- Primero
- Segundo
  - Tercero
    - Cuarto
- Quinto

1. Primero
2. Segundo
   1. Tercero
      1. Cuarto
3. Quinto

## TABLAS
---
Para crear una tabla hay que a�adir tantos | | como columnas se quieran, y en la siguiente fila, tantos |-| como haya en la fila de arriba. En las filas posteriores, siempre que las filas est�n seguidas (sin filas vac�as), todo lo que se encuentre entre dos | ser� tomado como columna de la tabla.

~~~~
|T�tulo 1|T�tulo 2|T�tulo 3|  
|-|-|-|  
|Elemento 1|||  
||Elemento 2||  
|||Elemento 3|
~~~~  

| T�tulo 1 | T�tulo 2 | T�tulo 3 |
|----------|----------|----------|
|Elemento 1|          |          |
|          |Elemento 2|          |
|          |          |Elemento 3|

Si se quiere desplazar el texto hacia la derecha, el centro o la izquierda, tan solo hay que sustituir el |-| de la segunda fila por |:-|, |:-:|, |-:| respectivamente.

~~~~
|Izquierda|Centro|Derecha|  
|:-|:-:|-:|  
|<--|<-->|-->|
~~~~ 

|Izquierda|Centro|Derecha|
|:--------|:----:|------:|
|<--      | <--> |    -->|

## CITAS
---
Para a�adir un texto en formato *cita*, se a�ade un *>* al principo del p�rrafo.

~~~~
> Cita
~~~~
> Cita


Dentro de una misma *cita* se pueden crear m�ltiples p�rrafos a�andiendo un > entre dos p�rrafos citados.

~~~~
> P�rrafo 1  
>  
> P�rrafo 2 
~~~~ 

> P�rrafo 1  
>
> P�rrafo 2  

Las *citas* se pueden anidar a�adiendo varios > seguidos en el siguiente p�rrafo. Si se pasa de escribir de un p�rrafo a uno de "mayor nivel", se debe dejar una l�nea en blanco con tantos > tenga el p�rrafo de mayor nivel.

~~~~
> P�rrafo 1  
>> Subp�rrafo 1.1  
>> Subp�rrafo 1.2   
>  
> P�rrafo 2  
>> Subp�rrafo 2.1  
>>> Subsubp�rrafo 2.1.1  
>  
> P�rrafo 3 
~~~~ 

> P�rrafo 1  
>> Subp�rrafo 1.1  
>> Subp�rrafo 1.2  
>
> P�rrafo 2  
>> Subp�rrafo 2.1  
>>> Subsubp�rrafo 2.1.1 
> 
> P�rrafo 3  

Las citas se pueden mezclar con otros elementos como el [�nfasis de texto](#�nfasis-de-texto), [listas](#listas) o [tablas](#tablas).

## C�DIGO
---
Escribir el c�digo deseado entre dos l�neas que contengan "~~~~". Para remarcar con colores el c�digo, se puede escribir el nombre del programa al que se hace referencia *(pascal, c, python, sql, ...)* seguido de la primera l�nea de virgulillas.

PASCAL:
~~~~ pascal
PROGRAM HOLAMUNDO;

USES Crt;

begin
    Write('Hola Mundo');
    ReadKey;
end.
~~~~

C:
~~~~ c
/*Programa: Hola Mundo*/

#include <conio.h>
#include <stdio.h>

int.main(){
    printf("Hola Mundo");
    return 0;
}
~~~~

Python:
~~~~ python
print("Hola Mundo")
~~~~

SQL:
~~~~ sql
SELECT Nombre, Apellido, Edad, DNI
  FROM TABLA.DATOS
 WHERE Edad BETWEEN 18 AND 35
   AND DNI LIKE '%X'
 ORDER BY DNI;
~~~~

> Todo lo que se escriba dentro de las virguilillas, *Markdown* lo escribir� directamente sin interpretaci�n de s�mbolos.

## LINKS
---

#### Enlaces web
Las ***URLs*** se pueden escribir directamente (o entre los s�mbolos <>) y *Markdown* los interpreta directamente como �nlaces.
~~~~
https://duckduckgo.com/
~~~~
https://duckduckgo.com/

Para convertir un texto en link solo hay que encerrarlo entre corchetes y seguido la ***URL*** entre par�ntesis.
~~~~
[Duck Duck Go](https://duckduckgo.com/)
~~~~
[Duck Duck Go](https://duckduckgo.com/)

Si se quiere que aparezca un peque�o t�tulo al dejar el rat�n sobre el �nlace, despu�s del enlace, escribir entre comillas el texto deseeado.
~~~~
[Duck Duck Go](https://duckduckgo.com/ "El mejor buscador para programaci�n")
~~~~
[Duck Duck Go](https://duckduckgo.com/ "El mejor buscador para programaci�n")

#### Llamada de encabezados
La llamada de un [encabezado](#encabezados) del propio documento se forma a partir de:
1. El texto que aparecer� en pantalla entre corchetes.
2. Entre par�ntesis, nombre del encabezados con guiones en vez espacios y una almohadilla (#) al principio.

~~~~
[Gu�a Markdown](#gu�a-markdown)
~~~~

[Gu�a Markdown](#gu�a-markdown)

> **NOTA:** las tildes en la llamada del nombre del encabezado no funcionan directamente en *Markdown*, pero s� en la preview de **Azure** o **GitHub**.

#### Referencias

Se trata de links especiales declarados dentro del propio documento de *Markdown*. Est�n formados a partir de dos partes:  
1. El texto entre corchetes que funcionar� a modo de �nlace y a su derecha, tambi�n entre corchetes, el nombre del �nlace referenciado definido aparte.
2. El �nlace definido con su nombre entre corchetes, dos puntos, espacio, ***URL*** � nombre de un encabezado, un t�tulo entre (), "" � '' (opcional)

~~~~
[URL][link 1]
[Encabezado][link 2]

[link 1]: https://www.google.es/ (buscador)
[link 2]: #�ndice "vuelta al principio"
~~~~
[URL][link 1]  
[Encabezado][link 2]

[link 1]: https://www.google.es/ (buscador)
[link 2]: #�ndice "vuelta al principio"

#### Documentos
El formato es parecido al de [enlaces web](#enlaces-web) pero esta vez poniendo la direcci�n del documento dentro de nuestros archivos o simplemente escribiendo el nombre del documento si se encuentra en la misma ruta que el archivo actual.
~~~~
[Manual de Python](ManualPython.md)
~~~~
[Manual de Python](ManualPython.md)

Si queremos ir a un apartado concreto del documento tan solo hay que aplicar la [llamada de encabezados](#llamada-de-encabezados) al final.
~~~~
[Manual de Python - Tipos de datos Primitivos Simples](ManualPython.md#tipos-de-datos-primitivos-simples)
~~~~
[Manual de Python - Tipos de datos Primitivos Simples](ManualPython.md#tipos-de-datos-primitivos-simples)
> Si el archivo al que queremos acceder se encuentra una o varias carpetas m�s atr�s, tan solo hay que poner *"../"* al comienzo de la ruta por cada carpeta que queramos retroceder.

#### Im�genes
Para agregar im�genes se tratar�a de un simbolo de exlamaci�n (!), nombre entre corchetes y la direcci�n en los documentos (sin espacios) o ***URL***
~~~~
![Foto](https://www.costacruzeiros.com/content/dam/costa/costa-magazine/articles-magazine/travel/croatia-travel/croazia_m.jpg.image.694.390.low.jpg "Croacia")
~~~~
![Foto](https://www.costacruzeiros.com/content/dam/costa/costa-magazine/articles-magazine/travel/croatia-travel/croazia_m.jpg.image.694.390.low.jpg "Croacia")

Para insertar un link a una im�gen ser�a combinar [enlaces web](#enlaces-web) e [im�genes](#im�genes).
~~~~
[![Esquema](https://upload.wikimedia.org/wikipedia/commons/a/a1/Alan_Turing_Aged_16.jpg "Alan Turing")](https://es.wikipedia.org/wiki/Alan_Turing)
~~~~
[![Esquema](https://upload.wikimedia.org/wikipedia/commons/a/a1/Alan_Turing_Aged_16.jpg "Alan Turing")](https://es.wikipedia.org/wiki/Alan_Turing)

## INHABILITACI�N DE COMANDOS MARKDOWN 
---
Si se quiere escribir un car�cter concreto sin que *Markdown* lo interprete solo hay que escribir una barra inversa (\\) a la izquierda del car�cter.
~~~~
\*\*Texto**
~~~~
\*\*Texto**