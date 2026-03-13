---
runtime: thorio
uses:
  - thorio
ide_web_runnable: true
ide_web_reason: "Usa solo el lenguaje base y puede ejecutarse en el IDE web."
---

# Ejemplo técnico 12 - Máximo y mínimo

Este ejemplo recorre una lista y calcula su valor máximo y mínimo.

Sirve para probar:

- inicialización desde la lista
- comparación repetida
- actualización condicional
- reutilización de funciones

```thorio
funcion maximo(valores: lista_entero) retorna entero
  definir indice como entero
  definir actual como entero

  indice = 1
  actual = valores[0]

  mientras indice < longitud(valores) hacer
    si valores[indice] > actual entonces
      actual = valores[indice]
    si_no
      actual = actual
    fin_si
    indice = indice + 1
  fin_mientras

  retornar actual
fin_funcion

funcion minimo(valores: lista_entero) retorna entero
  definir indice como entero
  definir actual como entero

  indice = 1
  actual = valores[0]

  mientras indice < longitud(valores) hacer
    si valores[indice] < actual entonces
      actual = valores[indice]
    si_no
      actual = actual
    fin_si
    indice = indice + 1
  fin_mientras

  retornar actual
fin_funcion

inicio
  definir datos como lista_entero

  datos = [14, 3, 27, 8, 19]

  mostrar "Lista: " + datos
  mostrar "Máximo: " + maximo(datos)
  mostrar "Mínimo: " + minimo(datos)
fin
```
