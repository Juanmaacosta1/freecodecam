# Revisión de Diccionarios y Conjuntos en Python

## Diccionarios

### ¿Qué es un diccionario?

Los **diccionarios** son estructuras de datos integradas en Python que almacenan **pares clave-valor**.

* Las **claves** deben ser tipos de datos **inmutables**.
* Permiten acceder rápidamente a los valores usando su clave.

### Sintaxis básica

```python
dictionary = {
    key1: value1,
    key2: value2
}
```

### Constructor `dict()`

Otra forma de crear un diccionario es usando el constructor `dict()` con una lista de tuplas.

```python
pizza = dict([
    ('name', 'Margherita Pizza'),
    ('price', 8.9),
    ('calories_per_slice', 250),
    ('toppings', ['mozzarella', 'basil'])
])
```

### Acceder a valores

Puedes acceder al valor de una clave usando **notación de corchetes**.

```python
dictionary[key]
```

---

# Métodos comunes de diccionarios

## Método `get()`

Recupera el valor asociado a una clave.
Permite definir un valor por defecto si la clave no existe.

```python
dictionary.get(key, default)
```

---

## Métodos `keys()` y `values()`

Devuelven un **objeto vista** con todas las claves o valores del diccionario.

```python
pizza = {
    'name': 'Margherita Pizza',
    'price': 8.9,
    'calories_per_slice': 250
}

pizza.keys()
# dict_keys(['name', 'price', 'calories_per_slice'])

pizza.values()
# dict_values(['Margherita Pizza', 8.9, 250])
```

---

## Método `items()`

Devuelve un objeto vista con **todos los pares clave-valor**.

```python
pizza.items()

# dict_items([
# ('name', 'Margherita Pizza'),
# ('price', 8.9),
# ('calories_per_slice', 250)
# ])
```

---

## Método `clear()`

Elimina **todos los elementos** del diccionario.

```python
pizza.clear()
```

---

## Método `pop()`

Elimina una clave específica y devuelve su valor.

```python
pizza.pop('price', 10)
pizza.pop('total_price')  # KeyError si no existe
```

---

## Método `popitem()`

Desde **Python 3.7**, elimina el **último elemento insertado**.

```python
pizza.popitem()
```

---

## Método `update()`

Actualiza el diccionario con los valores de otro diccionario.

```python
pizza.update({
    'price': 15,
    'total_time': 25
})
```

---

# Iterar sobre diccionarios

## Iterar sobre valores

```python
products = {
    'Laptop': 990,
    'Smartphone': 600,
    'Tablet': 250,
    'Headphones': 70,
}

for price in products.values():
    print(price)
```

Resultado:

```
990
600
250
70
```

---

## Iterar sobre claves

```python
for product in products.keys():
    print(product)

# o directamente

for product in products:
    print(product)
```

Resultado:

```
Laptop
Smartphone
Tablet
Headphones
```

---

## Iterar sobre claves y valores

```python
for product in products.items():
    print(product)
```

Resultado:

```
('Laptop', 990)
('Smartphone', 600)
('Tablet', 250)
('Headphones', 70)
```

Para separar la clave y el valor:

```python
for product, price in products.items():
    print(product, price)
```

Resultado:

```
Laptop 990
Smartphone 600
Tablet 250
Headphones 70
```

---

# Función `enumerate()`

Permite iterar con un **contador automático**.

```python
for index, product in enumerate(products.items()):
    print(index, product)
```

Resultado:

```
0 ('Laptop', 990)
1 ('Smartphone', 600)
2 ('Tablet', 250)
3 ('Headphones', 70)
```

También puedes definir el número inicial:

```python
for index, product in enumerate(products.items(), 1):
    print(index, product)
```

Resultado:

```
1 ('Laptop', 990)
2 ('Smartphone', 600)
3 ('Tablet', 250)
4 ('Headphones', 70)
```

---

# Conjuntos (Sets)

## ¿Qué es un conjunto?

Los **conjuntos** son estructuras de datos que:

* **No permiten elementos duplicados**
* Son **mutables**
* **No tienen orden**
* Solo contienen **tipos de datos inmutables**

---

## Crear un conjunto

```python
my_set = {1, 2, 3, 4, 5}
```

---

## Conjunto vacío

Para crear un conjunto vacío debes usar `set()`.

```python
set()  # Set vacío
{}     # Diccionario vacío
```

---

# Métodos comunes de conjuntos

## Método `add()`

Agrega un elemento al conjunto.

```python
my_set.add(6)
```

---

## Métodos `remove()` y `discard()`

Eliminan elementos del conjunto.

```python
my_set.remove(4)   # Error si no existe
my_set.discard(4)  # No genera error
```

---

## Método `clear()`

Elimina todos los elementos.

```python
my_set.clear()
```

---

# Operaciones matemáticas con conjuntos

## `issubset()` y `issuperset()`

```python
my_set = {1, 2, 3, 4, 5}
your_set = {2, 3, 4, 5}

print(your_set.issubset(my_set))   # True
print(my_set.issuperset(your_set)) # True
```

---

## `isdisjoint()`

Verifica si dos conjuntos **no tienen elementos en común**.

```python
my_set = {1, 2, 3}
your_set = {4, 5, 6}

print(my_set.isdisjoint(your_set))  # True
```

---

## Unión `|`

Combina todos los elementos de ambos conjuntos.

```python
my_set | your_set
```

Resultado:

```
{1, 2, 3, 4, 5, 6}
```

---

## Intersección `&`

Devuelve los elementos en común.

```python
my_set & your_set
```

Resultado:

```
{2, 3, 4}
```

---

## Diferencia `-`

Devuelve los elementos del primer conjunto que no están en el segundo.

```python
my_set - your_set
```

Resultado:

```
{1, 5}
```

---

## Diferencia simétrica `^`

Elementos que están en **uno u otro conjunto pero no en ambos**.

```python
my_set ^ your_set
```

Resultado:

```
{1, 5, 6}
```

---

## Operador `in`

Verifica si un elemento pertenece al conjunto.

```python
print(5 in my_set)
```

---

# Biblioteca estándar de Python

La **biblioteca estándar** contiene módulos con código reutilizable como:

* `math`
* `random`
* `re`
* `datetime`

Estos módulos incluyen funciones, clases y utilidades listas para usar.

---

# Declaración `import`

Para usar un módulo se utiliza la palabra clave **import**.

```python
import module_name
```

Luego se accede a sus funciones usando notación de punto.

```python
module_name.method_name()
```

Ejemplo:

```python
import math

math.sqrt(36)
```

---

# Importar con alias

Puedes usar un alias con `as`.

```python
import math as m

m.sqrt(36)
```

---

# Importar elementos específicos

```python
from module_name import name1, name2
```

Ejemplo:

```python
from math import radians, sin, cos

angle_degrees = 40
angle_radians = radians(angle_degrees)

print(sin(angle_radians))
print(cos(angle_radians))
```

También puedes usar alias:

```python
from module_name import name1 as alias1
```

---

# Importar todo (`*`)

```python
from module_name import *
```

Esto permite usar funciones sin el prefijo del módulo.

```python
from math import *

print(sqrt(36))
```

⚠️ No es recomendable porque puede causar **conflictos de nombres**.

---

# `if __name__ == "__main__"`

`__name__` es una variable especial en Python.

* Cuando ejecutas un archivo directamente → `__name__ = "__main__"`
* Cuando el archivo se importa como módulo → `__name__` es el nombre del módulo.

Por eso se usa esta estructura:

```python
if __name__ == '__main__':
    # código que se ejecuta solo si el archivo es el programa principal
```
