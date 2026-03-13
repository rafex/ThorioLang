---
runtime: thorio
uses:
  - thorio
ide_web_runnable: true
ide_web_reason: "Usa solo el lenguaje base y puede ejecutarse en el IDE web."
---

# Ejemplo técnico 09 - Funciones y listas

Este ejemplo combina dos de las capacidades nuevas del lenguaje:

- funciones declaradas antes de `inicio`
- listas tipadas
- acceso por indice
- builtin `longitud(...)`

```thorio
funcion ultimoElemento(valores: lista_entero) retorna entero
  retornar valores[longitud(valores) - 1]
fin_funcion

inicio
  definir numeros como lista_entero

  numeros = [4, 8, 15, 16]

  mostrar "Cantidad: " + longitud(numeros)
  mostrar "Ultimo: " + ultimoElemento(numeros)

  numeros[1] = 99
  mostrar "Lista final: " + numeros
fin
```
