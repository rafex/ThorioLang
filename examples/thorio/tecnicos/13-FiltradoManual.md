---
runtime: thorio
uses:
  - thorio
ide_web_runnable: true
ide_web_reason: "Usa solo el lenguaje base y puede ejecutarse en el IDE web."
---

# Ejemplo técnico 13 - Filtrado manual con listas

Este ejemplo construye una segunda lista copiando solo los valores mayores o iguales a 10.

Sirve para probar:

- listas preinicializadas
- escritura por índice
- contador separado para resultados válidos
- filtrado manual sin sintaxis especial

```thorio
inicio
  definir origen como lista_entero
  definir filtrados como lista_entero
  definir indice como entero
  definir posicion como entero

  origen = [4, 10, 7, 12, 15]
  filtrados = [0, 0, 0, 0, 0]
  indice = 0
  posicion = 0

  mientras indice < longitud(origen) hacer
    si origen[indice] >= 10 entonces
      filtrados[posicion] = origen[indice]
      posicion = posicion + 1
    si_no
      posicion = posicion
    fin_si
    indice = indice + 1
  fin_mientras

  mostrar "Origen: " + origen
  mostrar "Filtrados (con espacios sobrantes): " + filtrados
  mostrar "Cantidad válida: " + posicion
fin
```
