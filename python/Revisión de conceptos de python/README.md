# Revisión de conceptos básicos de Python

## ¿Qué es Python?

Python es un **lenguaje de programación de propósito general** conocido por su simplicidad y facilidad de uso. Se utiliza en muchos campos como:

* Ciencia de datos
* Aprendizaje automático
* Desarrollo web
* Automatización y scripting
* Sistemas embebidos e IoT

### Casos de uso comunes

Python se utiliza ampliamente en:

* Ciencia de datos
* Machine Learning
* Desarrollo web
* Ciberseguridad
* Automatización
* Microcomputadores como **Raspberry Pi** y dispositivos compatibles con **MicroPython**

---

# Python en tu entorno local

## Instalación

La forma recomendada de instalar Python en **Windows, Mac y Linux** es descargando el instalador desde el sitio oficial:

https://www.python.org/

---

# Variables

## Declaración de variables

Para declarar una variable se usa el **operador de asignación (=)**.

Ejemplo:

```python
name = 'John Doe'
age = 25
```

## Convenciones para nombrar variables

* Deben comenzar con una **letra o guion bajo (_)**.
* No pueden comenzar con un número.
* Solo pueden contener **caracteres alfanuméricos y guiones bajos**.
* Son **sensibles a mayúsculas y minúsculas**.
* No pueden usar **palabras reservadas** como `if`, `class` o `def`.
* Para varias palabras se usa **snake_case**.

Ejemplo:

```
user_name
total_price
student_age
```

---

# Comentarios

## Comentarios de una línea

Se utilizan para notas cortas dentro del código.

```python
# This is a single line comment
```

## Cadenas multilínea

Se utilizan para notas más extensas o para comentar bloques de código.

```python
"""
This is a multi-line string.
Here is some code commented out.

name = 'John Doe'
age = 25
"""
```

---

# Función print()

Se usa para **mostrar información en la consola**.

```python
print('Hello world!')
```

Salida:

```
Hello world!
```

---

# Tipos comunes de datos en Python

Python es un lenguaje de **tipado dinámico**, por lo que no es necesario declarar el tipo de una variable explícitamente.

## Entero (int)

```python
my_integer_var = 10
print('Integer:', my_integer_var)
```

## Flotante (float)

```python
my_float_var = 4.50
print('Float:', my_float_var)
```

## Cadena (str)

```python
my_string_var = 'hello'
print('String:', my_string_var)
```

## Booleano (bool)

```python
my_boolean_var = True
print('Boolean:', my_boolean_var)
```

## Conjunto (set)

```python
my_set_var = {7, 5, 8}
print('Set:', my_set_var)
```

## Diccionario (dict)

```python
my_dictionary_var = {"name": "Alice", "age": 25}
print('Dictionary:', my_dictionary_var)
```

## Tupla (tuple)

```python
my_tuple_var = (7, 5, 8)
print('Tuple:', my_tuple_var)
```

## Rango (range)

```python
my_range_var = range(5)
print(my_range_var)
```

## Lista (list)

```python
my_list = [22, 'Hello world', 3.14, True]
print(my_list)
```

## None

Representa **ausencia de valor**.

```python
my_none_var = None
print('None:', my_none_var)
```

---

# Tipos mutables e inmutables

## Tipos inmutables

No pueden cambiar después de ser creados.

Ejemplos:

* int
* float
* bool
* str
* tuple
* range
* None

## Tipos mutables

Pueden modificarse después de su creación.

Ejemplos:

* list
* set
* dict

---

# Funciones type() e isinstance()

## type()

Permite conocer el tipo de una variable.

```python
greeting = 'Hello there!'
age = 21

print(type(greeting))
print(type(age))
```

## isinstance()

Verifica si una variable es de un tipo específico.

```python
print(isinstance('Hello world', str))
print(isinstance('John Doe', int))
```

---

# Trabajo con cadenas de caracteres

Las **cadenas (strings)** son **inmutables**, lo que significa que no se pueden modificar después de crearlas.

```python
developer = 'Jessica'
city = 'Los Angeles'
```

---

# Acceso a caracteres

Se usa la notación de **corchetes []**.

```python
my_str = "Hello world"

print(my_str[0])
print(my_str[6])

print(my_str[-1])
print(my_str[-2])
```

---

# Escape de cadenas

Se usa `\` para escapar caracteres especiales.

```python
msg = 'It\'s a sunny day'
quote = "She said, \"Hello!\""
```

---

# Concatenación de cadenas

Usando `+`:

```python
developer = 'Jessica'
print('My name is ' + developer + '.')
```

Usando `+=`:

```python
greeting = 'My name is '
developer = 'Jessica.'

greeting += developer
print(greeting)
```

---

# f-strings

Permiten insertar variables dentro de cadenas.

```python
developer = 'Jessica'
greeting = f'My name is {developer}.'

print(greeting)
```

---

# Segmentación de cadenas (Slicing)

Sintaxis:

```
str[start:stop:step]
```

Ejemplo:

```python
message = 'Python is fun!'

print(message[0:6])
print(message[7:])
print(message[::2])
```

---

# Longitud de una cadena

```python
developer = 'Jessica'

print(len(developer))
```

---

# Operador in

Permite verificar si un elemento está dentro de una cadena.

```python
my_str = 'Hello world'

print('Hello' in my_str)
print('hey' in my_str)
print('e' in my_str)
```

---

# Métodos comunes de cadenas

### upper()

```python
developer = 'Jessica'
print(developer.upper())
```

### lower()

```python
print(developer.lower())
```

### strip()

```python
greeting = '  hello world  '
print(greeting.strip())
```

### replace()

```python
greeting = 'hello world'
print(greeting.replace('hello', 'hi'))
```

### split()

```python
dashed_name = 'example-dashed-name'
print(dashed_name.split('-'))
```

### join()

```python
example_list = ['example', 'dashed', 'name']
print(' '.join(example_list))
```

### startswith()

```python
developer = 'Naomi'
print(developer.startswith('N'))
```

### endswith()

```python
developer = 'Naomi'
print(developer.endswith('N'))
```

### find()

```python
developer = 'Naomi'
print(developer.find('N'))
```

### count()

```python
city = 'Los Angeles'
print(city.count('e'))
```

### capitalize()

```python
dessert = 'chocolate cake'
print(dessert.capitalize())
```

### isupper() / islower()

```python
print(dessert.isupper())
print(dessert.islower())
```

### title()

```python
city = 'los angeles'
print(city.title())
```

---

# Operaciones con números

## Operaciones básicas

```python
int_1 = 56
int_2 = 12

print(int_1 + int_2)
print(int_1 - int_2)
print(int_1 * int_2)
print(int_1 / int_2)
```

---

# Operadores matemáticos

### Módulo (%)

```python
print(56 % 12)
```

### División entera (//)

```python
print(56 // 12)
```

### Exponente (**)

```python
print(4 ** 2)
```

---

# Funciones numéricas útiles

### float()

```python
print(float(4))
```

### int()

```python
print(int(4.0))
```

### round()

```python
print(round(3.4))
```

### abs()

```python
print(abs(-13))
```

### bin(), oct(), hex()

```python
print(bin(56))
print(oct(56))
print(hex(56))
```

---

# Funciones

Las **funciones** son bloques reutilizables de código.

```python
def get_sum(num_1, num_2):
    return num_1 + num_2

result = get_sum(3, 4)
print(result)
```

Si una función no retorna nada explícitamente, devuelve `None`.

---

# Funciones con valores por defecto

```python
def get_sum(num_1, num_2=2):
    return num_1 + num_2
```

---

# Función input()

Permite recibir datos del usuario.

```python
name = input('What is your name?')
print('Hello', name)
```

---

# Alcance de variables (Scope)

## Local

Dentro de una función.

## Envolvente

Variables accesibles dentro de funciones anidadas.

## Global

Variables declaradas fuera de funciones.

## Incorporado

Funciones y objetos propios de Python.

---

# Operadores de comparación

```python
==   Igual
!=   Diferente
>    Mayor que
<    Menor que
>=   Mayor o igual
<=   Menor o igual
```

Ejemplo:

```python
print(3 == 4)
print(3 != 4)
```

---

# Condicionales

## if

```python
if age >= 18:
    print('You are an adult')
```

## elif

```python
elif age >= 13:
    print('You are a teenager')
```

## else

```python
else:
    print('You are a child')
```

---

# Valores verdaderos y falsos

Valores considerados **False**:

```
None
False
0
0.0
''
```

Otros valores generalmente se consideran **True**.

---

# Función bool()

Convierte valores a booleanos.

```python
print(bool(0))
print(bool('Hello'))
```

---

# Operadores booleanos

## and

```python
if is_citizen and age >= 18:
    print('You are eligible to vote')
```

## or

```python
if age < 18 or is_student:
    print('You are eligible for a student discount')
```

## not

```python
if not is_admin:
    print('Access denied')
```

---

# Cortocircuito

Los operadores **and** y **or** utilizan **evaluación de cortocircuito**, lo que significa que Python deja de evaluar cuando ya conoce el resultado final.
