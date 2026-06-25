# Musical Instrument

Ejercicio simple de programación orientada a objetos en Python.

Se creó una clase llamada `MusicalInstrument` que permite representar distintos instrumentos musicales mediante su nombre y familia de instrumentos.

## Funcionalidades

* Crear instrumentos con nombre y tipo.
* Mostrar un mensaje indicando que el instrumento se está tocando.
* Obtener información sobre la familia a la que pertenece el instrumento.

## Ejemplo

```python
instrument_1 = MusicalInstrument("Oboe", "woodwind")
instrument_2 = MusicalInstrument("Trumpet", "brass")

instrument_1.play()
print(instrument_1.get_fact())
```

## Objetivo

Practicar conceptos básicos de programación orientada a objetos en Python, incluyendo:

* Clases
* Objetos
* Métodos
* Constructores (`__init__`)
* Uso de `self`
* Retorno de valores con `return`
