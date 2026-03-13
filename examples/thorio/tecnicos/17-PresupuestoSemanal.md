---
runtime: thorio
uses:
  - thorio
ide_web_runnable: true
ide_web_reason: "Usa solo el lenguaje base y puede ejecutarse en el IDE web."
---

# Presupuesto semanal

Usa funciones, listas y comparaciones para resumir gastos.

```thorio
funcion total_gastos(gastos: lista_decimal) retorna decimal
  definir indice como entero
  definir suma como decimal

  indice = 0
  suma = 0.0

  mientras indice < longitud(gastos) hacer
    suma = suma + gastos[indice]
    indice = indice + 1
  fin_mientras

  retornar suma
fin_funcion

inicio
  definir gastos como lista_decimal
  definir presupuesto como decimal
  definir total como decimal

  gastos = [15.5, 20.0, 8.5, 12.0, 18.0]
  presupuesto = 80.0
  total = total_gastos(gastos)

  mostrar "Gastos: " + gastos
  mostrar "Total: " + total

  si total <= presupuesto entonces
    mostrar "Presupuesto bajo control"
  si_no
    mostrar "Presupuesto excedido"
  fin_si
fin
```
