---
runtime: thorio
uses:
  - thorio
ide_web_runnable: true
ide_web_reason: "Usa solo el lenguaje base y puede ejecutarse en el IDE web."
---

# Ejemplo técnico 15 - Inventario simple

Este ejemplo usa dos listas paralelas: una para nombres y otra para existencias.

Sirve para probar:

- listas de texto y entero
- actualización de stock por índice
- recorrido y presentación de registros relacionados

```thorio
funcion totalExistencias(stock: lista_entero) retorna entero
  definir indice como entero
  definir total como entero

  indice = 0
  total = 0

  mientras indice < longitud(stock) hacer
    total = total + stock[indice]
    indice = indice + 1
  fin_mientras

  retornar total
fin_funcion

inicio
  definir productos como lista_texto
  definir stock como lista_entero
  definir indice como entero

  productos = ["Cuaderno", "Lápiz", "Borrador"]
  stock = [12, 30, 8]

  stock[1] = stock[1] - 5
  stock[2] = stock[2] + 10

  indice = 0

  mientras indice < longitud(productos) hacer
    mostrar productos[indice] + ": " + stock[indice]
    indice = indice + 1
  fin_mientras

  mostrar "Total en inventario: " + totalExistencias(stock)
fin
```
