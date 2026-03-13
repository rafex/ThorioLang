---
runtime: thorio
uses:
  - thorio
ide_web_runnable: true
ide_web_reason: "Usa solo el lenguaje base y puede ejecutarse en el IDE web."
---

# Ejemplo técnico 11 - Búsqueda en lista

Este ejemplo recorre una lista para buscar un valor objetivo.

Sirve para probar:

- recorrido por índice
- comparación dentro de un ciclo
- retorno temprano desde funciones
- uso de valores lógicos

```thorio
funcion contiene(valores: lista_entero, objetivo: entero) retorna logico
  definir indice como entero

  indice = 0

  mientras indice < longitud(valores) hacer
    si valores[indice] == objetivo entonces
      retornar verdadero
    si_no
      indice = indice + 1
    fin_si
  fin_mientras

  retornar falso
fin_funcion

inicio
  definir datos como lista_entero

  datos = [3, 7, 11, 18, 21]

  mostrar "Lista: " + datos
  mostrar "¿Contiene 11? " + contiene(datos, 11)
  mostrar "¿Contiene 5? " + contiene(datos, 5)
fin
```
