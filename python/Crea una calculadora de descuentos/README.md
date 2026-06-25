# Laboratorio: Calculadora de Descuentos - apply_discount()

Este repositorio contiene una función en Python llamada `apply_discount` diseñada para calcular el precio final de un artículo después de aplicarle un porcentaje de descuento. El proyecto incluye validaciones exhaustivas de datos para garantizar la robustez del código.

##  Descripción

La función `apply_discount(price, discount)` toma el precio original de un artículo y el porcentaje de descuento a aplicar, y devuelve el precio final. Incluye múltiples comprobaciones para manejar errores comunes de entrada.

**Ejemplo de uso:**
Si el precio de un artículo es 50 y se aplica un descuento del 20%, el monto del desccuento es 10 y el precio final es 40.

##  Funcionalidades

La función está diseñada para cumplir con los siguientes casos de uso:

1.  **Definición correcta:** Existe una función llamada `apply_discount`.
2.  **Parámetros correctos:** La función acepta exactamente dos parámetros: `price` y `discount`.
3.  **Validación del precio (tipo):** Si `price` no es un número (`int` o `float`), retorna `"The price should be a number"`.
4.  **Validación del descuento (tipo):** Si `discount` no es un número (`int` o `float`), retorna `"The discount should be a number"`.
5.  **Validación del precio (valor):** Si `price` es menor o igual a 0, retorna `"The price should be greater than 0"`.
6.  **Validación del descuento (rango):** Si `discount` es menor que 0 o mayor que 100, retorna `"The discount should be between 0 and 100"`.
7.  **Cálculo preciso:** Si ambas entradas son válidas, calcula el descuento como porcentaje del precio y devuelve el precio final.

##  Instalación y Uso

### Prerrequisitos
- Python 3.x instalado en tu sistema.

### Cómo usar

1.  Clona este repositorio (o descarga el archivo `Laboratorio.py`).
    ```bash
    git clone [URL de tu repositorio]
    cd [nombre del directorio]
    ```
2.  Importa la función en tu script de Python o pruébala directamente en la consola interactiva.

