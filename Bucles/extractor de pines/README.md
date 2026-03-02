# 🧩 Extractor de Pines

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.x-blue?style=for-the-badge&logo=python" alt="Python">
  <img src="https://img.shields.io/badge/Estado-Funcionando-success?style=for-the-badge" alt="Estado">
  <img src="https://img.shields.io/badge/Licencia-MIT-yellow?style=for-the-badge" alt="Licencia">
</p>

<p align="center">
  <b>🔍 Extrae códigos secretos ocultos en poemas • Ideal para aprender Python • Fácil de usar</b>
</p>

---

## 📖 ¿Qué es esto?

**Extractor de Pines** es un proyecto en Python que analiza poemas para descifrar códigos secretos ocultos en las longitudes de las palabras. ¿Un poema con un mensaje oculto? Sí, cada línea guarda un dígito del pin, y este programa sabe exactamente dónde buscar.

> "Entre versos y metáforas, los números esperan ser descubiertos"

---

##  ¿Cómo funciona?

Cada línea del poema guarda un dígito. La regla es simple:
- **Cada línea del poema contiene un dígito del pin**
- El dígito n-ésimo del pin es la **longitud de la palabra n-ésima** en la línea n-ésima
- El índice de la línea determina qué palabra usar (primera línea → primera palabra, segunda línea → segunda palabra, etc.)
- Si una línea no tiene suficientes palabras, simplemente se omite

| Línea | Palabra que se mira | Lo que obtienes |
|-------|---------------------|-----------------|
| 0 | Primera palabra | Su longitud = 1er dígito |
| 1 | Segunda palabra | Su longitud = 2do dígito |
| 2 | Tercera palabra | Su longitud = 3er dígito |
| ... | ... | ... |

**¿Qué pasa si una línea tiene pocas palabras?**  
El programa es inteligente y simplemente salta esa línea. ¡Nadie se entera!

---

## 🕵️‍♂️ ¿Cómo funciona el programa?

El programa paso a paso:
-  Toma uno o varios poemas
-  Divide cada poema en líneas usando `\n`
-  En cada línea, selecciona una palabra específica (la que está en la misma posición que el número de línea)
- Mide la longitud de esa palabra con `len()`
-  Concatena todas las longitudes para formar un código numérico
- 📋Devuelve una lista con los pines de todos los poemas procesados

---