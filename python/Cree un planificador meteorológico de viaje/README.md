# 🌤️ Travel Weather Planner

<img src="https://img.shields.io/badge/Python-3.x-blue.svg" alt="Python Version">

Laboratorio de programación que utiliza **declaraciones condicionales** para determinar la viabilidad de un viaje basado en condiciones meteorológicas, distancia y disponibilidad de vehículos.

---

## 📋 Descripción

En este laboratorio crearás un planificador meteorológico de viaje utilizando declaraciones condicionales (`if`, `elif`, `else`) para evaluar diferentes escenarios de desplazamiento en función del clima, la distancia a recorrer y la disponibilidad de un vehículo.

**Objetivo:** Completar las historias de usuario y obtener todas las pruebas aprobadas para finalizar el laboratorio.

---

## 🔧 Variables Requeridas

| Variable | Tipo | Descripción |
|:---------|:-----|:------------|
| `distance_mi` | `número` | Distancia a recorrer en millas |
| `is_raining` | `booleano` | Indica si está lloviendo actualmente |
| `has_bike` | `booleano` | Indica si el usuario tiene bicicleta |
| `has_car` | `booleano` | Indica si el usuario tiene automóvil |
| `has_ride_share_app` | `booleano` | Indica si el usuario tiene app de viaje compartido |

---

## 🧠 Reglas de Decisión

### 📏 Evaluación por Rango de Distancia (en orden ascendente)

| Rango | Condición para Viajar |
|:-----:|:----------------------|
| **Valor falso** | `False` directamente |
| **≤ 1 milla** | `True` si **NO llueve**<br>`False` si llueve |
| **1 < d ≤ 6 millas** | `True` si tiene **bicicleta** Y **NO llueve**<br>`False` en cualquier otro caso |
| **> 6 millas** | `True` si tiene **auto** O **app de viaje compartido**<br>`False` si no tiene ninguno |

---

## ✅ Lista de Verificación

### Variables
- [ ] 1. Tener una variable llamada `distance_mi`
- [ ] 2. Asignar un número a `distance_mi`
- [ ] 3. Tener una variable llamada `is_raining`
- [ ] 4. Asignar un valor booleano a `is_raining`
- [ ] 5. Tener una variable llamada `has_bike`
- [ ] 6. Asignar un valor booleano a `has_bike`
- [ ] 7. Tener una variable llamada `has_car`
- [ ] 8. Asignar un valor booleano a `has_car`
- [ ] 9. Tener una variable llamada `has_ride_share_app`
- [ ] 10. Asignar un valor booleano a `has_ride_share_app`

### Estructuras de Control
- [ ] 11. Usar al menos una sentencia `if`
- [ ] 12. Usar al menos una rama `elif`
- [ ] 13. Usar al menos un operador booleano (`and`, `or`, `not`)
- [ ] 14. Usar la función `print()` para mostrar el resultado

---

## 🧪 Casos de Prueba Esperados

| # | Distancia | 🌧️ Lluvia | 🚲 Bicicleta | 🚗 Auto | 📱 App | Resultado Esperado |
|:-:|:---------:|:---------:|:------------:|:-------:|:------:|:------------------:|
| 15 | ≤ 1 milla | No | - | - | - | `True` |
| 16 | ≤ 1 milla | Sí | - | - | - | `False` |
| 17 | 1-6 millas | Sí | Sí | - | - | `False` |
| 18 | 1-6 millas | No | No | - | - | `False` |
| 19 | 1-6 millas | No | Sí | - | - | `True` |
| 20 | > 6 millas | - | - | No | Sí | `True` |
| 21 | > 6 millas | - | - | Sí | No | `True` |
| 22 | > 6 millas | - | - | No | No | `False` |

---

## 📝 Notas Importantes

- Debes utilizar declaraciones condicionales para determinar si es posible realizar desplazamientos
- Evalúa las categorías de distancia en orden ascendente
- Si `distance_mi` es un valor falso, imprime `False` directamente
- Todos los resultados deben mostrarse con la función `print()`

---

## 🎯 ¡Completa el laboratorio!

Asegúrate de que tu programa pase todos los casos de prueba del 1 al 22 para completar exitosamente el laboratorio.