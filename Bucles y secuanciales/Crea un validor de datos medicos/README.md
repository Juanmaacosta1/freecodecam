# Medical Records Validation – Python

Este proyecto implementa un pequeño sistema en **Python** para almacenar y validar registros médicos de pacientes.

## 1. Creación de la estructura de datos

Se declara una variable llamada `medical_records` y se le asigna una **lista vacía**. Esta lista se utilizará para almacenar datos médicos de pacientes.

Cada elemento de la lista será un **diccionario** que representa un paciente.

Se agrega un diccionario con la siguiente estructura:

* `patient_id`: `"P1001"`
* `age`: `34`
* `gender`: `"Female"`
* `diagnosis`: `"Hypertension"`
* `medications`: `['Lisinopril']`
* `last_visit_id`: `"V2301"`

Siguiendo esta estructura, la lista `medical_records` puede contener datos de otros pacientes.

---

# 2. Creación de la función de validación

Se crea una función llamada `validate` con un parámetro llamado `data`.

La función se encargará de validar el formato de los datos recibidos.

## Verificación del tipo de datos

Dentro de la función se crea la variable:

`is_sequence`

Esta variable utiliza `isinstance()` para verificar que `data` sea una **lista o una tupla**.

Si `data` **no es una lista o tupla**, se imprime:

```
Invalid format: expected a list or tuple.
```

y la función retorna `False`.

---

# 3. Verificación de diccionarios dentro de la lista

Se declara la variable:

`is_invalid = False`

Luego se crea un **ciclo for** usando `enumerate()` para obtener:

* `index`
* `dictionary`

Si el elemento no es un diccionario se imprime:

```
Invalid format: expected a dictionary at position <index>.
```

y `is_invalid` se establece en `True`.

Después del ciclo se verifica:

Si `is_invalid` es `True`, la función retorna `False`.

---

# 4. Validación de claves del diccionario

Se crea un conjunto llamado `key_set` con las claves esperadas:

```
['patient_id', 'age', 'gender', 'diagnosis', 'medications', 'last_visit_id']
```

Dentro del ciclo `for`, se verifica que el conjunto de claves del diccionario coincida con `key_set`.

Si las claves son incorrectas o faltan claves, se imprime:

```
Invalid format: <dictionary> at position <index> has missing and/or invalid keys.
```

y `is_invalid` se establece en `True`.

---

# 5. Pruebas de validación

Se llama a la función:

```
validate(medical_records)
```

Si todo es correcto se debería imprimir:

```
Valid format.
```

También se pueden hacer pruebas cambiando el tipo de `medical_records` a una cadena o agregando elementos que no sean diccionarios para verificar los mensajes de error.

---

# 6. Función para validar valores individuales

Se crea una función llamada:

`find_invalid_records`

Esta función recibe los parámetros:

* `patient_id`
* `age`
* `gender`
* `diagnosis`
* `medications`
* `last_visit_id`

Dentro de la función se crea un diccionario vacío llamado:

`constraints`

Este diccionario almacenará los resultados de cada validación.

---

# 7. Validación de `patient_id`

Se verifica que `patient_id` sea una **cadena** usando `isinstance`.

Además, se valida que tenga el formato correcto usando **expresiones regulares**.

Para esto se importa el módulo:

```
import re
```

El patrón utilizado verifica que el identificador tenga:

* la letra `P`
* seguida de **uno o más dígitos**

Ejemplo de patrón:

```
P\d+
```

Se utiliza `re.fullmatch()` junto con `re.IGNORECASE`.

---

# 8. Validación de `age`

Se verifica que:

* sea un **entero**
* sea **mayor o igual a 18**

Esto se logra usando `isinstance(age, int)` y una segunda condición con el operador `and`.

---

# 9. Validación de `gender`

Se verifica que:

* sea una cadena
* su valor en minúsculas esté en:

```
('male', 'female')
```

---

# 10. Validación de `diagnosis`

Se comprueba que el valor sea:

* una cadena (`str`)
* o `None`.

---

# 11. Validación de `medications`

Se verifica que:

* sea una **lista**

Luego se usa una **comprensión de listas** para comprobar que cada elemento sea una cadena.

```
[isinstance(i, str) for i in medications]
```

Después se utiliza la función `all()` para asegurarse de que todos los valores sean `True`.

---

# 12. Validación de `last_visit_id`

Se verifica que `last_visit_id` sea una **cadena** usando `isinstance`.

---

# 13. Identificación de claves inválidas

La función `find_invalid_records` devuelve una **lista con las claves inválidas**.

Esto se realiza usando una **comprensión de listas** que recorre `constraints.items()` y agrega la clave solo si su valor es `False`.

---

# 14. Uso de la función dentro de `validate`

Dentro del ciclo `for` de la función `validate`, se crea la variable:

`invalid_records`

Esta variable llama a:

```
find_invalid_records(**dictionary)
```

El operador `**` se usa para **desempaquetar el diccionario** y pasar sus valores como argumentos.

---

# 15. Manejo de errores durante la validación

Si los datos contienen errores como:

* elementos que no son diccionarios
* diccionarios con claves faltantes

Python puede generar errores como:

* `AttributeError`
* `TypeError`

Para evitar esto, después de detectar un error se utiliza:

```
continue
```

Esto permite saltar a la siguiente iteración del ciclo y continuar la validación.
