# 🔢 Number Pattern Generator

Este proyecto consiste en la creación de una función en Python llamada `number_pattern` que genera un patrón numérico en forma de cadena.

## 📌 Descripción

La función recibe un número entero positivo `n` y devuelve una cadena con todos los números desde **1 hasta n**, separados por un espacio.

Ejemplo:

```python
number_pattern(4)
```

Salida:

```
1 2 3 4
```

---

##  Requisitos del Ejercicio

La función debe cumplir con las siguientes condiciones:

* Debe llamarse `number_pattern`.
* Debe recibir un solo parámetro llamado `n`.
* Debe utilizar un bucle `for`.
* Debe devolver una cadena con números desde `1` hasta `n` separados por espacios.
* Si el argumento no es un número entero, debe devolver:

  ```
  Argument must be an integer value.
  ```
* Si el número es menor que 1, debe devolver:

  ```
  Argument must be an integer greater than 0.
  ```

---


##  Conceptos Practicados

* Definición de funciones
* Validación de tipos con `isinstance()`
* Uso de bucle `for`
* Uso de `range()`
* Conversión de datos con `str()`
* Manipulación de cadenas con `join()`

---

## 📚 Objetivo 

Este ejercicio refuerza los fundamentos de Python relacionados con estructuras de control, validación de datos y construcción de cadenas dinámicas.

Es ideal para principiantes que están comenzando a practicar lógica de programación en Python.
