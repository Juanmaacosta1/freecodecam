# ⚔️ RPG Character Builder

Proyecto desarrollado como parte de mi práctica en Python dentro del módulo de Fundamentos.

En este laboratorio construí una función que permite crear un personaje para una aventura RPG validando correctamente el nombre y las estadísticas iniciales.

---

## 🎯 Objetivo

Implementar una función llamada `create_character` que:

- Reciba un nombre y tres estadísticas:
  - Strength
  - Intelligence
  - Charisma
- Valide correctamente todos los datos de entrada
- Devuelva una representación visual del personaje usando puntos (● y ○)

---

## 🧠 Reglas del sistema

### Validaciones del nombre

El personaje:

- Debe ser un string
- No puede estar vacío
- No puede tener más de 10 caracteres
- No puede contener espacios

---

### Validaciones de estadísticas

Las estadísticas:

- Deben ser números enteros
- Deben estar entre 1 y 4
- La suma total debe ser exactamente 7 puntos

Esto simula un sistema clásico de distribución de puntos iniciales en juegos RPG.

---

## 🖥️ Ejemplo de uso

```python
create_character("ren", 4, 2, 1)