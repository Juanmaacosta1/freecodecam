# User Configuration Manager

Este proyecto implementa un **Gestor de Configuración de Usuario** en Python.
Permite administrar diferentes configuraciones de un usuario como el **tema, idioma, notificaciones y volumen** mediante operaciones básicas sobre un diccionario.

El proyecto fue desarrollado como parte de un laboratorio de práctica de **Python**, donde se implementan funciones para **agregar, actualizar, eliminar y visualizar configuraciones**.

---

#  Objetivo

Construir un sistema simple que permita administrar configuraciones de usuario utilizando estructuras de datos de Python (diccionarios) y funciones.

Las funcionalidades incluyen:

* Agregar configuraciones
* Actualizar configuraciones existentes
* Eliminar configuraciones
* Visualizar configuraciones actuales

---

# ⚙️ Funciones Implementadas

## 1️⃣ add_setting(settings, setting)

Agrega una nueva configuración al diccionario.

**Parámetros**

* `settings`: diccionario con configuraciones actuales
* `setting`: tupla `(key, value)`

**Comportamiento**

* Convierte `key` y `value` a minúsculas
* Si la clave ya existe, devuelve un mensaje de error
* Si la clave no existe, agrega el par clave-valor al diccionario

**Ejemplo**

```python
add_setting({'theme': 'light'}, ('volume', 'high'))
```

Resultado:

```
Setting 'volume' added with value 'high' successfully!
```

---

## 2️⃣ update_setting(settings, setting)

Actualiza el valor de una configuración existente.

**Parámetros**

* `settings`: diccionario de configuraciones
* `setting`: tupla `(key, value)`

**Comportamiento**

* Convierte `key` y `value` a minúsculas
* Si la clave existe, actualiza el valor
* Si la clave no existe, devuelve un mensaje de error

**Ejemplo**

```python
update_setting({'theme': 'light'}, ('theme', 'dark'))
```

Resultado:

```
Setting 'theme' updated to 'dark' successfully!
```

---

## 3️⃣ delete_setting(settings, key)

Elimina una configuración existente.

**Parámetros**

* `settings`: diccionario de configuraciones
* `key`: nombre de la configuración

**Comportamiento**

* Convierte la clave a minúsculas
* Si existe, elimina la configuración
* Si no existe, devuelve un mensaje de error

**Ejemplo**

```python
delete_setting({'theme': 'light'}, 'theme')
```

Resultado:

```
Setting 'theme' deleted successfully!
```

---

## 4️ view_settings(settings)

Muestra todas las configuraciones almacenadas.

**Parámetros**

* `settings`: diccionario de configuraciones

**Comportamiento**

* Si el diccionario está vacío devuelve:

```
No settings available.
```

* Si contiene configuraciones, las muestra en el siguiente formato:

```
Current User Settings:
Theme: dark
Notifications: enabled
Volume: high
```

---

#  Datos de prueba

Para probar el sistema se utiliza el siguiente diccionario:

```python
test_settings = {
    "theme": "dark",
    "notifications": "enabled",
    "volume": "high"
}
```

---

#  Conceptos de Python utilizados

Este proyecto utiliza varios conceptos fundamentales de Python:

* Diccionarios (`dict`)
* Tuplas (`tuple`)
* Funciones
* Condicionales (`if`)
* Métodos de strings (`lower()`, `capitalize()`)
* Iteración con `for`
* Formato de strings (`f-strings`)

---

# 📂 Estructura del proyecto

```
user-config-manager
│
├── main.py
└── README.md
```

---

#  Cómo ejecutar el proyecto

1. Clonar el repositorio

```bash
git clone https://github.com/tu-usuario/tu-repositorio.git
```

2. Ejecutar el archivo Python

```bash
python main.py
```

---

# 📚 Autor

Proyecto desarrollado por **Juanma Acosta** como práctica de programación en Python.
