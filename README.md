# Programación de Computadores - UNAL
## Condicionales

## Estructura if
La estructura de control condicional o de selecci´on permite ejecutar, o un  grupo de instrucciones u otro grupo si una condici´on se cumple.

Cuando en el flujo de un programa se desea que se ejecute un grupo de instrucciones cuando un condicional se evalu´e verdadero, y que se continue con la ejecuci´on del resto del programa se haya o no ejecutado la instrucciones del condicional, se tiene un caso de condicional sin opci´on alternativa.

Este tipo de estructura se suele utilizar cuando se desea agregar una evaluaci´on intermedia de una expresi´on cuando la condici´on se eval´ua verdadero, pero que no tiene impacto sobre la ejecuci´on del resto del programa que le sigue al condicional.

**Diagrama de flujo**
```
flowchart TD;
  A[bloque_previo] --> B{condicion}
  B --Sí--> C[bloque_verdadero]
  B --> D[bloque_siguiente]
  C --> D
```

**Pseudocódigo**
```pseudocode
bloque_previo
si (condicion) entonces
  bloque_verdadero
bloque_siguiente
```

**python**
```python
<bloque_previo>
if <condicion>:
  <bloque_verdadero>
bloque_siguiente
```

**Ejemplo:** Dado un número n (entero), imprima un mensaje si está entre 2 y 5, al final imprima el número.
```python
n : int = 4
if n >= 2 and n <= 5:
  print("El numero " + str(n)+ " esta entre 2 y 5")
print(n)
```
### Ingreso de datos
Es bastante común ingresar datos a un programa. Para ingresar información por consola se utiliza la función *input()*.

```python
<var> = input("prompt")
```

**Ejemplo:** Ingrese un número n (entero), imprima un mensaje si está entre 2 y 5, al final imprima el número.

```python
n : int 
n = int(input("Ingrese un numero entero: ")) # Conversion a entero
if n >= 2 and n <= 5:
  print("El numero " + str(n)+ " esta entre 2 y 5")
print(n)
```
**Pro tip:** Por defecto *input()* trae un *string*, por lo tanto es necesario hacer la conversión al tipo de dato deseado.

## Estructura if-else
La estructura de control condicional o de selecci´on permite ejecutar, o un  grupo de instrucciones u otro grupo si una condici´on se cumple o no.

**Diagrama de flujo**
```
flowchart TD;
  A[bloque_previo] --> B{condicion}
  B --Sí--> C[bloque_verdadero]
  B --No--> D[bloque_falso]
  C --> E[bloque_siguiente]
  D --> E
```

**Pseudocódigo**
```pseudocode
bloque_previo
si (condicion) entonces
  bloque_verdadero
sino 
  bloque_falso
bloque_siguiente
```

**python**
```python
<bloque_previo>
if <condicion>:
  <bloque_verdadero>
else:
  <bloque_falso>
bloque_siguiente
```

**Ejemplo:** Ingrese un número n (entero), imprima un mensaje si está entre 2 y 5, en caso contrario imprima un mensaje que indique si es menor a 2 o mayor a 5, al final imprima el número.

```python
n : int 
n = int(input("Ingrese un numero entero: ")) # Conversion a entero
if n >= 2 and n <= 5:
  print("El numero " + str(n)+ " esta entre 2 y 5")
else:
  if n < 2:
    print("El numero " + str(n)+ " es menor que 2")
  if n > 5:
    print("El numero " + str(n)+ " es mayor que 5")
print(n)
```

**Ejemplo:** Ingrese un dos números (a,b) e imprima cúal es el mayor, si son iguales imprima ambos números.
```python
a : float
b : float
a = float(input("Ingrese el primer numero: ")) 
b = float(input("Ingrese el segundo numero: ")) 
if a == b:
  print(a,b)
else:
  if a > b:
    print(a)
  if b > a:
    print(b)
```
**Ejemplo:** Ingrese un número y determine si es positivo o negativo.
```python
a : float
a = float(input("Ingrese un numero: ")) 
if a >= 0:
  print("El numero "+str(a)+" es positivo")
else:
  print("El numero "+str(a)+" es negativo")
```

**Ejemplo:** Ingrese un número y retorne su valor absoluto.
```python
a : float
a = float(input("Ingrese un numero: ")) 
if a >= 0:
  print("El valor absoluto es "+str(a))
else:
  print("El valor absoluto es "+str(-a))
```

### Condicional ternarario
Es uan forma de abreviar el condicional cuando solo cuenta con una instrucción en el bloque de ejecución.

Retomando el ejemplo del valor absoluto.
```python
a : float
valor_abs : float
a = float(input("Ingrese un numero: ")) 
valor_abs = a if a >= 0 else -a
print("El valor absoluto es "+str(valor_abs))
```

## Estructura if-elif-else
Otra de las opciones para utilizar una estructura condicional es la de enlazar varias estructuras condicionales, de tal manera que solamente se pueda ejecutar un grupo de instrucciones dependiendo de cual de las opciones se eval´ua verdadero. De la misma manera que en el caso del condicional tradicional la parte alternativa del final es opcional.

**Diagrama de flujo**
```
flowchart TD;
  A[bloque_previo] --> B{condicion_1}
  B --Sí--> C[bloque_verdadero_1]
  B --No--> D{condicion_2}
  D --Sí--> E[bloque_verdadero_2]
  D --No--> G{condición_n-1}
  G --Sí--> H[bloque_verdadero_n-1]
  G --No--> J[bloque_falso]
  C --> I[bloque_siguiente]
  E --> I
  H --> I
  J --> I
```

**Pseudocódigo**
```pseudocode
bloque_previo
si (condicion) entonces
  bloque_verdadero
sino 
  bloque_falso
bloque_siguiente
```

**python**
```python
<bloque_previo>
if <condicion>:
  <bloque_verdadero>
else:
  <bloque_falso>
bloque_siguiente
```

## Estructura match (switch)

## Anidación

