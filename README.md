# Manual de la prueba de acceso para el Bootcamp de Data Analytics de Ironhack


## Propósito de este documento

Con este documento pretendemos darte una ayuda para que pases la prueba técnica de acceso al bootcamp de Ironhack en análisis de datos y sepas a lo que te vas a enfrentar. Consistirá principalmente en resolver un problema básico de programación en Python. Los conceptos estadísticos necesarios serán mínimos.

Contiene tres secciones: 
* **Programación online**: para que practiques los ejemplos. 
* **Conocimientos de Python**: para que sepas los conocimientos mínimos con ejemplos. 
* **Ejemplo de prueba de acceso**: para que veas qué puedes encontrarte. 


## Programación online

Para que puedas programar sin tener que instalarte ningún software, hazte una cuenta en **repl**. Podrás practicar todo lo que quieras en muchos lenguajes de programación además de Python. Intenta probar a programar todo lo que se muestra en este documento. 

https://repl.it/repls

Sólo debes poner código en la sección blanca y darle al botón verde RUN.
![repl](./images/repl-example.png) 

## Conocimientos de Python

Para pasar la prueba deberás tener unos conocimientos mínimos

### Output
Para mostrar por pantalla un mensaje. 
```python
print("Hello World")
```

### Variables
Para asignar variables. 
```python
mensaje = "Hello World"
print(mensaje)
```

```python
a = 40
b = 2
z = a + b
print(z)
```

### Doing Math
Python es una calculadora supervitaminada. 
```python
suma = 39 + 3
resta = 15 - 13
multiplicacion = 12 * 2
division = 7 / 3
division_entera = 7 // 3

print(suma)
print(resta)
print(multiplicacion)
print(division)
print(division_entera)
```

### Input
Para escribir con el teclado y que la máquina lo almacene. Luego podremos usarlo y mostrarlo por pantalla si queremos. 
```python
nombre = input("Escribe tu nombre: ")
print("Hola", nombre, "!")
```


### String and Numeric Data Types
Para ver el tipo de variable que estamos usando: entero, número con decimales, cadena de carácteres, lista, etc. 
```python
# cadena de carácteres
cadena = "Esto es una cadena de carácteres"
tipo_cadena = type(cadena)
print(tipo_cadena)

# entero
entero = 42
tipo_entero = type(entero)
print(tipo_entero)

# entero
flotante = 42.42
tipo_flotante = type(flotante)
print(tipo_flotante)

# lista
lista = [1,2,3,4,5,1,2,3,4,5]
tipo_lista = type(lista)
print(tipo_lista)
```

### Counting and Indexing
Para ver la longitud de algo que se pueda recorrer: lista, cadena de carácteres, tupla, diccionario, etc.
Para seleccionar un elemento por su índice
```python
hechizo = "expeliarmus"
print(len(hechizo))
print(hechizo[0])
print(hechizo[1])
print(hechizo[-1])
```

### List
La salsa de python. Las listas no tienen límite. 
```python
# Ejemplos de listas. 
numeros = [3,4,3,5,7,4,3,1,1]
ninjas = ['Naruto', 'Sakura', 'Sasuke', 'Hinata', 'Shikamaru']
mezcla = ['apple', 390, 876, 'orange', 'highway', 0.42, 87]
matriz = [[3,4,5], [1,2,3], [7,3,2]]

# Para seleccionar un elemento por su índice
print(ninjas[0])
print(ninjas[-1])
print(matriz[0])

# lista[start: stop: step]
print(ninjas[::2])
print(ninjas[1: 4])
print(ninjas[::-1])

# añadir un elemento nuevo al final de un lista
print(ninjas)
ninjas.append('Kakashi')
print(ninjas)

# sumar listas
estudiantes = ['Harry', 'Hermione', 'Ron']
profesores = ['Dumbledore', 'Severus', 'Hagrid']
print(estudiantes)
print(profesores)
hogwards = estudiantes + profesores
print(hogwards)

### media de un conjunto de números
numeros = [34, 12, 93, 783, 330, 896, 1, 55]
suma = sum(numeros)
longitud = len(numeros)
media = suma / longitud
print(media)

### mínimo y máximo
minimo = min(numeros)
maximo = max(numeros)
print(minimo)
print(maximo)

### Ordenación
numeros_ordenados = sorted(numeros)
print(numeros_ordenados)
```

### Conjuntos
Los conjuntos son agrupaciones de elementos pero no se almacenan repetidos. 
```python
lista_peliculas_cine = ['Alien', 'Terminator 2', 'Arma Letal', 'Alien', 'Terminator 2']
opciones_peliculas = set(lista_peliculas_cine)
print(lista_peliculas_cine)
print(opciones_peliculas)
```

### Diccionarios
```python
valoraciones = {'Alien':9.5, 'Terminator 2':8.9, 'Arma Letal':7.3}

print(valoraciones['Alien'])
print(valoraciones.keys())
print(valoraciones.values())
print(valoraciones.items())
```

### Boolean Data Types
_Ser o no ser._ `True o False`
```python
print(5 + 5 == 10)
print('isla' != 'pantano')
print(100 >= 75)
print(93 <= 80)

# para ver si un elemento se encuentra en un conjunto o lista
print(3 in [1,2,3,4,5])
print(3 not in [1,2,3,4,5])

print((5 + 5 == 10) and ('isla' != 'pantano'))
print((100 > 75) and (93 < 80))
print((100 > 75) or (93 < 80))
print((93 < 80) or (3 not in [1,2,3,4,5]))
```
### Conditional (If / elif / else)
Para tomar decisiones
```python
entrada = input("Introduce un número entero: ")
# convertimos la cadena de carácteres en entero. Esta operación se llama cast. 
numero = int(entrada)

# Ahora veamos que has puesto
if numero == 42: 
	print("Has elegido 42")
elif numero < 42: 
	print("El número es menor que 42")
else: 
	print("El número es mayor que 42")
```

### Looping with Python
Para automatizarlo todo. 
```python
# Primer ejemplo: range
for numero in range(10):
	print(numero)

# Segundo ejemplo: range(start: stop: step)
for numero in range(5, 15, 2):
	print(numero)

# Tercer ejemplo
ninjas = ['Naruto', 'Sakura', 'Sasuke', 'Hinata', 'Shikamaru']
for ninja in ninjas: 
	print(ninja)

# Cuarto ejemplo
valoraciones = {'Alien':9.5, 'Terminator 2':8.9, 'Arma Letal':7.3}
for peli, puntuacion in valoraciones.items(): 
	print(peli, "tiene una puntuacion de", puntuacion)

# Quinto ejemplo: cálculo de la suma
numeros = [34, 12, 93, 783, 330, 896, 1, 55]
total = 0
for numero in numeros: 
	total += numero
print(total)

# Sexto ejemplo: 
lista = []
for x in range(2, 6): 
	numero = x**2
	lista.append(numero)
print(lista)
```


Lo de Yonatan
```python
# 1º crear una lista del 1 al 10​

lst=[1,2,3,4,5,6,7,8,9,10]      # version newbie
print (lst)

​lst=[i for i in range(1, 11)]   # version pro
print (lst)

# 2º crear una nueva lista desde la primera de los numeros pares o impares
# pares 

lst2=[]

for e in lst:                   # version newbie

	if e%2==0: lst2.append(e)

print (lst2)


lst2=[e for e in lst if e%2==0] # version pro

print (lst2)

​

# impares

lst2=[]

for e in lst:                  # version newbie

	if e%2==1: lst2.append(e)

print (lst2)

​

​

lst2=[e for e in lst if e%2==1] # version pro

print (lst2)

​

​

# 3º cambiar pares/impares por 0-1

​

# pares==0, impares==1

​

lst3=[]

for e in lst:                   # version newbie

	if e%2==0: lst3.append(0)

	else: lst3.append(1)

print (lst3)

​

​

lst3=[0 if e%2==0 else 1 for e in lst]  # version pro

print (lst3)

​

​

# pares==1, impares==0

​

lst3=[]

for e in lst:                     # version newbie

	if e%2==0: lst3.append(1)

	else: lst3.append(0)

print (lst3)

​

​

lst3=[1 if e%2==0 else 0 for e in lst]  # version pro

print (lst3)

​

​

​

​

# 4º sumar todos los elementos de la primera lista (dos versiones)

​

suma=0           # version 1

for e in lst:

	suma+=e

print (suma)

​

​

suma=sum(lst)    # version 2

print (suma)



```

## Ejemplo de prueba de acceso

A continuación hay una muestra de la antígua prueba de nivel. Ya no se pide esto pero te puede dar una idea de lo que se te preguntará. Recomendamos que intentes resolver este problema antes de presentarte a la prueba. 

Dada una lista de números enteros: 
1. Muestra por pantalla los números de esta lista que son mayores que 5.

```python
numeros = [1, 7, 6, 5, 4, 3, 2, 3, 4, 5, 6, 7, 6, 5, 4, 3, 2, 3, 4, 5, 6, 7]

for numero in numeros: 
	if numero > 5: 
		print(numero)
```

Obtendremos a la salida lo siguiente: 

```python
7 
6 
6 
7 
6 
6 
7
```

2. Indica cuántos números de la lista son mayores que 5.

```python
numeros = [1, 7, 6, 5, 4, 3, 2, 3, 4, 5, 6, 7, 6, 5, 4, 3, 2, 3, 4, 5, 6, 7]

mayores = 0
for numero in numeros: 
	if numero > 5: 
		mayores = mayores + 1

print(mayores)
```

Obtendremos a la salida lo siguiente: 

```python
7
```

3. Muestra por pantalla una nueva lista que traduzca los elementos de la lista original:
	* Los menores o iguales que 5 serán 0,
	* Los mayores que 5 serán 1.
```python
numeros = [1, 7, 6, 5, 4, 3, 2, 3, 4, 5, 6, 7, 6, 5, 4, 3, 2, 3, 4, 5, 6, 7]
solucion = []

for numero in numeros: 
	if numero > 5: 
		solucion.append(1)
	else: 
		solucion.append(0)

print(solucion)
```

Obtendremos a la salida lo siguiente: 

```python
[0, 1, 1, 0, 0, 0, 0, 0, 0, 0, 1, 1, 1, 0, 0, 0, 0, 0, 0, 0, 1, 1]
```
