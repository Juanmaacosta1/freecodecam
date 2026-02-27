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

