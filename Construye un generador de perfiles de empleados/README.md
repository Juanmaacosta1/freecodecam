# 👨‍💼 Proyecto: Gestión de Información de Empleados

Este repositorio contiene una implementación en Python para gestionar y formatear información de empleados. El proyecto explora conceptos fundamentales de manejo de cadenas, concatenación, f-strings, slicing y conversión de tipos.

## 📋 Descripción

El proyecto simula la creación de una tarjeta de información de empleado (`employee_card`) que contiene datos como nombre, edad, puesto, salario y código de empleado. A través de ejercicios progresivos, se aprenden técnicas esenciales para manipular texto en Python.

**Objetivos del proyecto:**
- Almacenar información de empleados usando variables.
- Formatear datos de manera legible y profesional.
- Extraer información específica de códigos usando slicing.
- Practicar la conversión de tipos para concatenación.

## 🚀 Funcionalidades

- **Concatenación básica:** Combinar nombres y apellidos para formar el nombre completo.
- **Concatenación con espacio:** Insertar correctamente espacios entre palabras.
- **Operador `+=`:** Agregar contenido adicional a una cadena existente.
- **Manejo de errores de tipo:** Convertir enteros a cadenas con `str()` para evitar `TypeError`.
- **f-strings (Python 3.6+):** Formateo moderno y legible de cadenas.
- **String slicing:** Extraer porciones específicas de códigos de empleado.
- **Indexación negativa:** Obtener caracteres desde el final de una cadena.

## 📦 Instalación y Uso

### Prerrequisitos
- Python 3.6 o superior (para soporte de f-strings).

### Cómo usar

1.  Clona este repositorio (o descarga el archivo `.py` correspondiente).
    ```bash
    git clone [URL de tu repositorio]
    cd [nombre del directorio]
    ```
2.  Ejecuta el script de Python.

```python
# Ejemplo de uso del código final
first_name = "John"
last_name = "Doe"
full_name = first_name + " " + last_name

employee_age = 28
position = "Data Analyst"
salary = 75000

# Usando f-strings para formatear
employee_card = f"Employee: {full_name} | Age: {employee_age} | Position: {position} | Salary: ${salary}"
print(employee_card)

# Extrayendo información de un código de empleado
employee_code = "DEV-2026-JD-001"
department = employee_code[0:3]      # "DEV"
year_code = employee_code[4:8]       # "2026"
initials = employee_code[9:11]        # "JD"
last_three = employee_code[-3:]       # "001"

print(f"Department: {department}, Year: {year_code}, Initials: {initials}, ID: {last_three}")