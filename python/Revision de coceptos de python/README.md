Revisión de conceptos básicos de Python
¿Qué es Python?
Introducción: Python es un lenguaje de programación de propósito general conocido por su simplicidad y facilidad de uso. Python se usa en muchos campos como la ciencia de datos y el aprendizaje automático, desarrollo web, secuencias de comandos y automatización, sistemas embebidos e IoT, y mucho más.
Casos de Uso Comunes: Python se usa en la ciencia de datos, el aprendizaje automático, el desarrollo web, la ciberseguridad, la automatización y microcomputadores como las plazas Raspberry Pi y compatibles con MicroPython.
Python en tu Entorno Local
Instalación: La mejor manera de instalar Python en Windows, Mac y Linux es descargar el instalador desde el sitio web oficial de Python (https://www.python.org/).
Variables
Declaración de variables: Para declarar una variable, comienza con el nombre de la variable seguido del operador de asignación (=) y luego el valor. Este puede ser un número, cadena, booleano, etc. Aquí hay ejemplos:
Código de ejemplo
name = 'John Doe'
age = 25
Convenciones para Nombrar Variables: Aquí están las convenciones de nombres que deben usar para variables:

Los nombres de las variables sólo puedo comer con una letra o un guion bajo (_) y no un número.
Los nombres de las variables sólo puedo tener caracteres alfanuméricos (az, AZ, 0-9) y guiones bajos (_).
Los nombres de las variables son sensibles a mayúsculas — edad, Edad, y EDAD se consideran únicos.
Los nombres de las variables no pueden ser una de las palabras clave reservadas de Python como if, class o def.
Los nombres de variables con múltiples palabras están separados por guiones bajos. Ej. snake_case.
Comentarios
Comentarios de Línea Única: Este tipo de comentarios debe utilizarse para notas cortas que desees dejar en tu código.
Código de ejemplo
# This is a single line comment
Cadenas multilínica: Este tipo de cadenas se pueden usar para dejar notas más extensas o para comentar secciones de código.
Código de ejemplo
"""
This is a multi-line string.
Here is some code commented out.

name = 'John Doe'
age = 25
"""
Función print(): Para imprimir datos en la consola, puedes usar la función print() de esta manera:
Código de ejemplo
print('Hello world!') # Hello world!
Tipos Comunes de Datos en Python
Introducción: Python es un lenguaje de tipado dinámico como JavaScript, lo que significa que no necesitas declarar explícitamente los tipos para las variables. El lenguaje sabe cuál es el tipo de una variable según lo que asuntos a la variable.
Entero: Un número entero sin decimales:
Código de ejemplo
my_integer_var = 10
print('Integer:', my_integer_var) # Integer: 10
Flotante: Un número con decimales:
Código de ejemplo
my_float_var = 4.50
print('Float:', my_float_var) # Float: 4.5
Cadena: Una seguridad de coches envuelta entre comillas:
Código de ejemplo
my_string_var = 'hello'
print('String:', my_string_var) # String: hello
Booleano: Un valor que representa True o False:
Código de ejemplo
my_boolean_var = True
print('Boolean:', my_boolean_var) # Boolean: True
Conjunto: Una colección desordenada de elementos únicos:
Código de ejemplo
my_set_var = {7, 5, 8}
print('Set:', my_set_var) # Set: {7, 5, 8}
Diccionario: Una colección de pares clave-valor encerrados entre llaves:
Código de ejemplo
my_dictionary_var = {"name": "Alice", "age": 25}
print('Dictionary:', my_dictionary_var) # Dictionary: {'name': 'Alice', 'age': 25}
Tupla: Una colección ordenada e inmutable, montada por parteesis:
Código de ejemplo
my_tuple_var = (7, 5, 8)
print('Tuple:', my_tuple_var) # Tuple: (7, 5, 8)
Rango: Una seguridad de números, que se usa a menos en bucles:
Código de ejemplo
my_range_var = range(5)
print(my_range_var) # range(0, 5)
Lista: Una colección ordenada de elementos que admiten diferentes tipos de datos:
Código de ejemplo
my_list = [22, 'Hello world', 3.14, True]
print(my_list) # [22, 'Hello world', 3.14, True]
Ninguno: Un valor especial que representa la ausencia de valor:
Código de ejemplo
my_none_var = None
print('None:', my_none_var) # None: None
Tipos Inmutables y Mutables
Tipos Inmutables: Estos tipos no pueden cambiar una vez declarados, une se puede redirigir sus variables a algo nuevo, lo que se llama reasignación. Incluyen entero, flotante, complejo, booleano, cadena, tupla, rango y Ninguno.
Tipos mutables: Estos tipos pueden cambiar una vez declarados. Puedes agregar, eliminar o actualizar sus elementos. Incluyen tipos de colección como listas, conjuntos y diccionarios.
Función type(): Para ver el tipo de una variable, puedes usar la función type() de esta manera:
Código de ejemplo
greeting = 'Hello there!'
age = 21

print(type(greeting)) # <class 'str'>
print(type(age)) # <class 'int'>
Función isinstance(): Se usa para verificar si una variable coincide con un tipo de dato específico:
Código de ejemplo
print(isinstance('Hello world', str)) # True
print(isinstance('John Doe', int)) # False
Trabajo con Cadenas de Caracteres
Definición: Como recuerdas de JavaScript, las cadenas de caracteres son inmutables, lo que significa que no puedes cambiarlas después de que se hayan creado. En Python, puedes usar comillas simples o dobles. Se recomienda elegir una regla y aprender a ella:
Código de ejemplo
developer = 'Jessica'
city = 'Los Angeles'
Acceso a Caracteres de Cadenas: Puedes acceder a caracteres de cadenas utilizando la notificación de corchetes de esta manera:
Código de ejemplo
my_str = "Hello world"

print(my_str[0])  # H
print(my_str[6])  # w

print(my_str[-1])  # d
print(my_str[-2]) # l
Escape de Cadenas: Puedes usar una barra invertida (\) si tu cadena cuenta comillas de esta manera:
Código de ejemplo
msg = 'It\'s a sunny day'
quote = "She said, \"Hello!\""
Concatenación de cadenas: Para concatenar cadenas, puedes usar el operador + de esta manera:
Código de ejemplo
developer = 'Jessica'
print('My name is ' + developer + '.') # My name is Jessica.
Otra forma de concatenar cadenas es usar el operador +=. Esto se usa para realizar la concatenación y la asignación en el mismo paso de esta manera:

Código de ejemplo
greeting = 'My name is '
developer = 'Jessica.'

greeting += developer
print(greeting) # My name is Jessica.
f-strings: Esta es una abreviatura para cadenas de formato literal. Te permite manejar la interpolación y también realizar la concatenación con una sintaxis compacta y legible:
Código de ejemplo
developer = 'Jessica'
greeting = f'My name is {developer}.'
print(greeting) # My name is Jessica.
Segmentación de Cadenas: Esto ocurre cuando puedes extraer partes de una cadena. Esta es la sintaxis básica:
Código de ejemplo
str[start:stop:step]
La posición de inicio representa el índice donde debe comer la extracción. La posición de parada es donde debe terminar el segmento. Esta posición no es inclusiva. La posición de paso representa el intervalo para el incremento en la segmentación. Aquí hay ejemplos:

Código de ejemplo
message = 'Python is fun!'

print(message[0:6])  # Python
print(message[7:])  # is fun!
print(message[::2])  # Pto sfn
Obtener la Longitud de una Cadena: La función len() se usa para desarrollar el número de caracteres en la cadena:
Código de ejemplo
developer = 'Jessica'

print(len(developer)) # 7
Trabajo con el Operador in
Operador in: Este desarrollo un booleano que específica si el personaje o los personajes existen en la cadena o no:
Código de ejemplo
my_str = 'Hello world'

print('Hello' in my_str)  # True
print('hey' in my_str)    # False
print('hi' in my_str)    # False
print('e' in my_str)  # True
print('f' in my_str)  # False
Métodos Comunes de Cadenas
str.upper(): Este desarrollo una nueva cadena con todos los personajes convertidos a mayúsculas:
Código de ejemplo
developer = 'Jessica'

print(developer.upper()) # JESSICA
str.lower(): Este desarrollo una nueva cadena con todos los personajes convertidos a minúsculas:
Código de ejemplo
developer = 'Jessica'

print(developer.lower()) # jessica
str.strip(): Este desarrollo una copia de la cadena con los personajes específicos al inicio y al final eliminados (si no se pasa un argumento al método, elimina los espacios en blanco al inicio y al final).
Código de ejemplo
greeting = '  hello world  '

trimmed_my_str = greeting.strip()
print(trimmed_my_str)  # 'hello world'
replace(): Este desarrollo una nueva cadena con todas las ocurrencias de la cadena antigua reemplazadas por una nueva.
Código de ejemplo
greeting = 'hello world'

replaced_my_str = greeting.replace('hello', 'hi')
print(replaced_my_str)  # 'hi world'
split(): Esto se usa para dividir una cadena en una lista usando un separador específico. Un separador es una cadena que indica dónde debe ocurrir la división.
Código de ejemplo
dashed_name = 'example-dashed-name'

split_words = dashed_name.split('-')
print(split_words)  # ['example', 'dashed', 'name']
join(): Esto se usa para unir elementos de un iterable en una cadena con un separador. Un iterable es una colección de elementos que se pueden recordar como una lista, cadena o una tupla.
Código de ejemplo
example_list = ['example', 'dashed', 'name']

joined_str = ' '.join(example_list)
print(joined_str)  # example dashed name
str.startswith(prefix): Este desarrollo un booleano que indica si una cadena viene con el prefijo específico:
Código de ejemplo
developer = 'Naomi'

result = developer.startswith('N')
print(result)  # True
str.endswith(suffix): Este desarrollo un booleano que indica si una cadena termina con el sufijo específico:
Código de ejemplo
developer = 'Naomi'

result = developer.endswith('N')
print(result)  # False
str.find(): Este desarrollo el índice de la primera aplicación de una subcadena. Si no se encuentra, se devolverá -1:
Código de ejemplo
developer = 'Naomi'

result = developer.find('N')
print(result)  # 0

city = 'Los Angeles'
print(city.find('New')) # -1
str.count(substring): Este cuenta cuentas vez aparece una subcadena en una cadena:
Código de ejemplo
city = 'Los Angeles'
print(city.count('e')) # 2
str.capitalize(): Este desarrollo una nueva cadena con el primer carácter en mayúscula y los demás en minúsculas:
Código de ejemplo
dessert = 'chocolate cake'
print(dessert.capitalize()) # Chocolate cake
str.isupper(): Esto devuelve True si todas las letras en la cadena están en mayúsculas y False si no:
Código de ejemplo
dessert = 'chocolate cake'
print(dessert.isupper()) # False
str.islower(): Esto devuelve True si todas las letras en la cadena están en minúsculas y False de lo contrario:
Código de ejemplo
dessert = 'chocolate cake'
print(dessert.islower()) # True
str.title(): Este desarrollo una nueva cadena con la primera letra de cada palabra en mayúscula:
Código de ejemplo
city = 'los angeles'
print(city.title()) # Los Angeles
str.maketrans(): Este método se usa para crear una tabla de mapeo de caracteres de uno a uno para la traducción. A menudo se usa con el método translate() que aplica esa tabla a una cadena y devuelve el resultado traducido.
Código de ejemplo
trans_table = str.maketrans('abc', '123')
print(trans_table) # {97: 49, 98: 50, 99: 51}

result = 'abcabc'.translate(trans_table)
print(result)  # 123123
Operaciones Comunas usadas con Enteros y Flotantes
Operaciones Matemáticas Básicas: En Python, puedes realizar operaciones matemáticas básicas con enteros y flotantes, incluido suma, resta, multiplicación y división:
Código de ejemplo
int_1 = 56
int_2 = 12
float_1 = 5.4
float_2 = 12.0

# Addition

print('Integer Addition:', int_1 + int_2) # Integer Addition: 68
print('Float Addition:', float_1 + float_2) # Float Addition: 17.4

# Subtraction

print('Int Subtraction:', int_1 - int_2) # Int Subtraction: 44
print('Float Subtraction:',  float_2 - float_1) # Float Subtraction: 6.6

# Multiplication

print('Int Multiplication:', int_1 * int_2) # Int Multiplication: 672
print('Float Multiplication:', float_2 * float_1) # Float Multiplication: 64.80000000000001

# Division

print('Int Division:', int_1 / int_2) # Int Division: 4.666666666666667
print('Float Division:', float_2 / float_1) # Float Division: 2.222222222222222
Cuando sumas un flotante y un entero, el resultado se convenientete en un flotante de esta manera:

Código de ejemplo
int_1 = 56
float_1 = 5.4

print(int_1 + float_1) # 61.4
Operador de Módulo (%): Este desarrollo el residuo cuando un número es dividido por otro número:
Código de ejemplo
int_1 = 56
int_2 = 12

print(int_1 % int_2) # 8
División de Piso (//): Este operador se usa para dividir dos números y redondear el resultado hasta abajo al número entero entero más cercano:
Código de ejemplo
int_1 = 56
int_2 = 12

print(int_1 // int_2) # 4
Operador de Exposición (**): Este operador se usa para elevar un número a la potencia de otro:
Código de ejemplo
int_1 = 4
int_2 = 2

print(int_1 ** int_2) # 16
Función float(): Puedes usar esta función para convertir un entero a flotante.
Código de ejemplo
num = 4

print(float(num)) # 4.0
Función int(): Puedes usar esta función para convertir un flotante a un entero.
Código de ejemplo
num = 4.0

print(int(num)) # 4
Función round(): Esto se utiliza para redondear un número al entero más cercano:
Código de ejemplo
num_1 = 3.4
num_2 = 7.7

print(round(num_1)) # 3
print(round(num_2)) # 8
Función abs(): Esto se usa para desarrollar el valor absoluto de un número:
Código de ejemplo
num = -13

print(abs(num)) # 13
Función bin(): Esto se usa para convertir un entero a su representación binaria como una cadena:
Código de ejemplo
num = 56

print(bin(num))  # 0b111000
Función oct(): Esto se usa para convertir un entero a su representación octal como una cadena:
Código de ejemplo
num = 56

print(oct(num))  # 0o70
Función hex(): Esto se usa para convertir un entero a su representación hexadecimal como una cadena:
Código de ejemplo
num = 56

print(hex(num))  # 0x38
Función pow(): Esto se utiliza para elevar un número a la potencia de otro:
Código de ejemplo
result = pow(2, 3) 
print(result)  # 8
Asignaciones Aumentadas
Definición: La asignación aumentada combinada una operación binaria con una asignación en un solo paso. Toma una variable, le aplica una operación con otro valor y alcalena el resultado nuevo en la misma variable.
Código de ejemplo
# Addition assignment 
my_var = 10
my_var += 5

print(my_var) # 15

# Subtraction assignment
count = 14
count -= 3

print(count) # 11

# Multiplication assignment 
product = 65
product *= 7

print(product) # 455

# Division assignment 
price = 100
price /= 4

print(price) # 25.0

# Floor Division assignment 
total_pages = 23
total_pages //= 5

print(total_pages) # 4

# Modulus assignment 
bits = 35
bits %= 2

print(bits) # 1

# Exponentiation assignment 
power = 2
power **= 3

print(power) # 8
También hay otros operadores de asignación aumentada, como los de operadores un poco. Incluyen &=, ^=, >>=, y <<=.

Trabajo con Funciones
Definición: Las funciones son piezas reutilizables de código que tomán entradas (argumentos) y devuelven una salida. Para llamar a una función, necesitamos hacer referencia al nombre de la función seguido de un conjunto de padresis:
Código de ejemplo
# Defining a function

def get_sum(num_1, num_2):
    return num_1 + num_2

result = get_sum(3, 4) # function call
print(result) # 7
Si una función no devuelve un valor explícitamente, comprende el valor de retorno predeterminado es Ninguno:

Código de ejemplo
def greet():
    print('hello') 

result = greet() # hello
print(result) # None
También podemos administrar valores predeterminados a los parámetros de esta manera:

Código de ejemplo
def get_sum(num_1, num_2=2):
    return num_1 + num_2

result = get_sum(3) 
print(result) # 5
Si llamas a la función sin el número correcto de argumentos, recibirás un TypeError:

Código de ejemplo
def calculate_sum(a, b):
    print(a + b)

calculate_sum()

# TypeError: calculate_sum() missing 2 required positional arguments: 'a' and 'b'
Funciones Integradas Comunas
Función input(): Esto se utiliza para pedir al usuario una entrada:
Código de ejemplo
name = input('What is your name?') # User types 'Kolade' and presses Enter  
print('Hello', name) # Hello Kolade
Función int(): Esto se utiliza para convertir un número, un booleano o una cadena numérica en un entero:
Código de ejemplo
print(int(3.14)) # 3
print(int('42')) # 42
print(int(True)) # 1
print(int(False)) # 0 
Alcance en Python
Ámbito Local: Esto sucedió cuando una variable declarada dentro de una función o clase solo puede acceder dentro de esa función o clase.
Código de ejemplo
def my_func():
    num = 10
    print(num)
Ámbito Envolvente: Esto sucedió cuando una función que está anidada dentro de otra función puede acceder a las variables de la función en la que está anidada.
Código de ejemplo
def outer_func():
    msg = 'Hello there!'
    
    def inner_func():
        print(msg)
    inner_func()

print(outer_func()) # Hello there!
Ámbito Global: Esto se refiere a variables que están declaradas fuera de cual función o clase, que pueden acceder desde cual lugar en el programa.
Código de ejemplo
tax = 0.70 

def get_total(subtotal):
    total = subtotal + (subtotal * tax)
    return total

print(get_total(100))  # 170.0
Ámbito Incorporado: Nombres reservados en Python para funciones, módulos, palabras clave y objetos predefinidos.
Código de ejemplo
print(str(45)) # '45'
print(type(3.14)) # <class 'float'>
print(isinstance(3, str)) # False
Operadores de Comparación
Igual (==): Comprueba si dos valores son iguales:
Código de ejemplo
print(3 == 4) # False
No igual (!=): Comprueba si dos valores no son iguales:
Código de ejemplo
print(3 != 4) # True
Estricto mayor que (>): Verifica si un valor es mayor que otro:
Código de ejemplo
print(3 > 4) # False
Estrictamente menor que (<): Verifica si un valor es menor que otro:
Código de ejemplo
print(3 < 4) # True
Mayor o igual que (>=): Verifica si un valor es mayor o igual que otro:
Código de ejemplo
print(3 >= 4) # False
Menor o igual(<=): Verifica si un valor es menor o igual que otro:
Código de ejemplo
print(3 <= 4) # True
Trabajo con instrucciones if, elif y else
Instrucciones if: Estas son condiciones utilizadas para determinar si algo es verdad o no. Si la condición evalúa a True, entre ese bloque de código se ejecuta.
Código de ejemplo
age = 18

if age >= 18:
    print('You are an adult') # You are an adult
Sentencia elif: Estas son condiciones que vienen despues de una sentencia if. Un bloque elif se ejecuta solo si todas las condiciones anteriores evalúan a False y su propiedad condición evalúa a True.
Código de ejemplo
age = 16

if age >= 18:
    print('You are an adult')
elif age >= 13:
    print('You are a teenager')  # You are a teenager
Cláusula else: Esto se ejecuta si ninguna otra condición se evalúa como True.
Código de ejemplo
age = 12

if age >= 18:
    print('You are an adult')
elif age >= 13:
    print('You are a teenager')
else:
    print('You are a child')  # You are a child
También puedes usar oraciones if anidades de esta manera:

Código de ejemplo
is_citizen = True
age = 25

if is_citizen:
    if age >= 18:
        print('You are eligible to vote') # You are eligible to vote
else:
    print('You are not eligible to vote')
Valores 'Verdaderos' y 'Falsos'
Definición: En Python, cada valor tiene un valor booleano inherente o un sentido incorporado de si debe tratarse como True o False en un contexto lógico. Muchos valores se consideran verdes, es decir, se evalúan como True en un contexto lógico. Otros son falsos, lo que significa que se evalúa como False. Aquí hay ejemplos de valores falsos:
Código de ejemplo
None
False
Integer 0
Float 0.0
Empty strings ''
Otros valores como nuevos distintos de cero y cadenas no vacaciones son verdes.

Entrenando con la función bool()
Definición: Si deseas comprar si un valor es verdad o falso, puedes usar la función bool() incorporada. Esta convenientete explícitamente un valor a su equivalente booleano y devuelve True para valores truthy y False para valores false. Aquí hay ejemplos:
Código de ejemplo
print(bool(False)) # False
print(bool(0))  # False
print(bool('')) # False

print(bool(True)) # True
print(bool(1)) # True
print(bool('Hello')) # True
Operadores Booleanos y Cortocircuito
Definición: Estos son operadores especiales que te permiten combinar múltiples expresiones para crear una lógica de toma de decisiones más completa en tu código. Hay tres operadores booleanos en Python: and, or y not.
and Operador: Este operador toma dos operadores y devuelve el primer operando si es falso, de lo contrario, devuelve el segundo operando. Ambos operadores deben ser verdad para que una expresión resulte en un valor verdad.
Código de ejemplo
is_citizen = True
age = 25

print(is_citizen and age) # 25
También puedes usar el operador and en condiciones así:

Código de ejemplo
is_citizen = True
age = 25

if is_citizen and age >= 18:
    print('You are eligible to vote') # You are eligible to vote
else:
    print('You are not eligible to vote')
or Operador: Este operador devuelve el primer operando si es verdadero, de lo contrario, devuelve el segundo operando. Una expresión o resultado en un valor verdadero si al menos un operando es verdadero. Aquí hay un ejemplo:
Código de ejemplo
age = 19
is_employed = False

print(age or is_employed) # 19
Al igual que con el operador and, puedes usar el operador or en condiciones así:

Código de ejemplo
age = 19
is_student = True

if age < 18 or is_student:
    print('You are eligible for a student discount') # You are eligible for a student discount
else:
    print('You are not eligible for a student discount')
Cortocircuito: Los operadores and y or se conocen como operadores de cortecircuito. El cortecircuito significa que Python verifica los valores de izquierda a derecha y se detiene tan pronto como determina el resultado final.
not Operador: Este operador toma un solo operando e invisible su valor booleano. Convierte valores truthy en False y valora falsy en True. A diferencia de los operadores anteriores que vimos, not siempre devuelve True o False. Aquí hay ejemplos:
Código de ejemplo
print(not '') # True, because empty string is falsy
print(not 'Hello') # False, because non-empty string is truthy
print(not 0) # True, because 0 is falsy
print(not 1) # False, because 1 is truthy
print(not False) # True, because False is falsy
print(not True) # False, because True is truthy
Aquí hay un ejemplo del operador not en incondicional:

Código de ejemplo
is_admin = False

if not is_admin:
    print('Access denied for non-administrators.') # Access denied for non-administrators.
else:
    print('Welcome, Administrator!')