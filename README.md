# Estructures_Dades_Sprint_2_T_M2_T01
Ejercicios de estructura de datos con Python.


## Ejercicio 1

### Crea una lista que agrrupe los meses del año en trimestres.


```python
trimestres =  {'1T':['Enero', 'Febrero', 'Marzo'],
          '2T':['Abril', 'Mayo', 'Junio'], 
          '3T':['Julio', 'Agosto', 'Septiembre'],
          '4T':['Octubre', 'Noviembre', 'Diciembre']}

trimestres
```




    {'1T': ['Enero', 'Febrero', 'Marzo'],
     '2T': ['Abril', 'Mayo', 'Junio'],
     '3T': ['Julio', 'Agosto', 'Septiembre'],
     '4T': ['Octubre', 'Noviembre', 'Diciembre']}



## Ejercicio 2

### Crea un codigo que te permita acceder a:

#### El segundo mes del primer trimestre.


```python

```


```python
print(trimestres['1T'][1])
```

    Febrero
    

#### Los meses del primer trimestre.


```python
print(trimestres['1T'])
```

    ['Enero', 'Febrero', 'Marzo']
    

#### Septiembre y Octubre


```python
print(trimestres['3T'][2],',', trimestres['4T'][0])
```

    Septiembre , Octubre
    

## Ejercicio 3

### Crea una lista con números desordenados.


```python
import random

lista_num = random.sample(range(1,50), 10)

print(lista_num)
```

    [37, 31, 47, 41, 13, 21, 9, 16, 49, 34]
    

### Responde las siguientes preguntas:

#### 1. ¿Cuántos números hay?


```python
cantidad_numeros = len(lista_num)
print(cantidad_numeros)
```

    10
    

#### 2. ¿Cuántas veces aparece el número 3?


```python
num_3 = lista_num.count(3)
print ('El número 3 aparece', num_3, 'veces en la lista.')
```

    El número 3 aparece 0 veces en la lista.
    

#### 3. ¿Cuantas veces aparecen los números 3 y 4?


```python
num_3 = lista_num.count(3)
num_4 = lista_num.count(4)

if num_3:
    print('El número 3 aparece', num_3, 'veces en la lista.')
elif num_4:
    print('El número 4 aparece', num_4, 'veces en la lista.')
else:
     print('Ni el 3, ni el 4 aparecen en la lista.')
```

    Ni el 3, ni el 4 aparecen en la lista.
    

#### 4. ¿Cuál es el número más alto?


```python
num_max = max(lista_num)
print(num_max)
```

    49
    

#### 5.¿Cuales son los tres números más pequeños?


```python
numeros_min = sorted(lista_num)
print(numeros_min[0:3])
```

    [9, 13, 16]
    

#### 6.¿Cuál es el rango de esta lista?


```python
for num in lista_num:
    maximo = lista_num[0]
    minimo = lista_num[0]
    if num < minimo:
        minimo = num
    if num > maximo:
        maximo = num

rango = maximo - minimo
        
print(rango)
```

    3
    

## Ejercicio 4

### Crea un diccionario.


```python
compra = { "Pomes" : {"Qty": 5, "€": 0.42}, 
          "Peres" : {"Qty": 3, "€": 0.66} }
```

### Responde las siguientes preguntas

#### Añade alguna fruta más


```python
compra["Toronjes"] = {'Qty': 8, '€': 0.23}
print(compra)
```

    {'Pomes': {'Qty': 5, '€': 0.42}, 'Peres': {'Qty': 3, '€': 0.66}, 'Toronjes': {'Qty': 8, '€': 0.23}}
    

#### ¿Cuánto han costado las peras en total?


```python
def calcular_precio (compra, fruta):
    return compra[fruta]['Qty'] * compra[fruta]['€']

Precio_total = calcular_precio(compra,'Peres')
print(Precio_total)
```

    1.98
    

#### ¿Cuántas frutas hemos comprado en total?


```python
def calcular_total_frutas (compra):
    total = 0
    for fruta in compra:
        total += compra[fruta]['Qty']
    return total
   

print(calcular_total_frutas(compra))
    
    
```

    16
    

#### ¿Cuál es la fruta más cara?


```python
def fruta_mas_cara(compra):
    fruta_cara= max(compra, key= lambda f: compra[f]['€'])
    return fruta_cara
    
fruta_cara = fruta_mas_cara(compra)
print (fruta_cara)
```

    Peres
    

# FIN
