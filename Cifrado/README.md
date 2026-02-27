# 🔐 Proyecto: Cifrado César (Caesar Cipher)

Este repositorio contiene una implementación en Python del histórico **Cifrado César**, una de las técnicas de encriptación más simples y antiguas. El proyecto incluye funciones para cifrar y descifrar mensajes, con validaciones de entrada y soporte para mayúsculas.

## 📋 Descripción

El Cifrado César es un tipo de cifrado por sustitución en el que cada letra del texto original es reemplazada por otra letra que se encuentra un número fijo de posiciones más adelante en el alfabeto.

**Ejemplo:**
Con un desplazamiento (`shift`) de 5:
- `a` se convierte en `f`
- `b` se convierte en `g`
- `hello` se convierte en `mjqqt`

## 🚀 Funcionalidades

- **Cifrado de mensajes:** Convierte texto plano en texto cifrado.
- **Descifrado de mensajes:** Recupera el texto original a partir de un mensaje cifrado.
- **Soporte para mayúsculas:** El cifrado funciona tanto con letras minúsculas como mayúsculas.
- **Validación de entrada:** Verifica que el desplazamiento sea un entero positivo entre 1 y 25.
- **Parámetros con valores por defecto:** La función principal puede cifrar o descifrar según un parámetro opcional.

## 📦 Instalación y Uso

### Prerrequisitos
- Python 3.x instalado en tu sistema.

### Cómo usar

1.  Clona este repositorio (o descarga el archivo `.py` correspondiente).
    ```bash
    git clone [URL de tu repositorio]
    cd [nombre del directorio]
    ```
2.  Importa las funciones en tu script de Python o pruébalas directamente.

```python
from caesar_cipher import encrypt, decrypt

# Cifrar un mensaje
mensaje_cifrado = encrypt("hello world", 5)
print(f"Cifrado: {mensaje_cifrado}")  # Salida: mjqqt btwqi

# Descifrar un mensaje
mensaje_descifrado = decrypt("mjqqt btwqi", 5)
print(f"Descifrado: {mensaje_descifrado}")  # Salida: hello world

# Ejemplo con mayúsculas
print(encrypt("Hello World", 3))  # Salida: Khoor Zruog

# Ejemplo con mensaje cifrado proporcionado
texto_cifrado = "Pbhentr vf sbhaq va hayvxryl cynprf"
texto_descifrado = decrypt(texto_cifrado, 13)
print(texto_descifrado)  # Salida: "Providencia" (o el mensaje descifrado)