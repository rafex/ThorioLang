---
runtime: thorio
uses:
  - thorio
ide_web_runnable: true
ide_web_reason: "Usa solo el lenguaje base y puede ejecutarse en el IDE web."
---

# Promedio de mediciones

Recorre una lista decimal para calcular un promedio.

```thorio
funcion promedio(valores: lista_decimal) retorna decimal
  definir indice como entero
  definir suma como decimal

  indice = 0
  suma = 0.0

  mientras indice < longitud(valores) hacer
    suma = suma + valores[indice]
    indice = indice + 1
  fin_mientras

  retornar suma / longitud(valores)
fin_funcion

inicio
  definir mediciones como lista_decimal

  mediciones = [18.5, 19.0, 20.0, 19.5]

  mostrar "Promedio: " + promedio(mediciones)
fin
```
