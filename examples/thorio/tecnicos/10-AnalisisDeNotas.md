---
runtime: thorio
uses:
  - thorio
ide_web_runnable: false
ide_web_reason: "Usa 'leer' y requiere entrada interactiva, por lo que no es apto para el IDE web actual."
---

# Ejemplo técnico 10 - Análisis de notas

Este ejemplo intenta explotar varias capacidades actuales de Thorio en un mismo programa:

- funciones
- listas tipadas
- acceso y actualización por índice
- `longitud(...)`
- condicionales
- ciclos `mientras`
- lectura desde entrada
- acumulación de resultados

La idea es leer tres notas, guardarlas en una lista y luego analizar el resultado.

```thorio
funcion sumarNotas(notas: lista_decimal) retorna decimal
  definir indice como entero
  definir suma como decimal

  indice = 0
  suma = 0

  mientras indice < longitud(notas) hacer
    suma = suma + notas[indice]
    indice = indice + 1
  fin_mientras

  retornar suma
fin_funcion

funcion promedioNotas(notas: lista_decimal) retorna decimal
  retornar sumarNotas(notas) / longitud(notas)
fin_funcion

funcion ultimaNota(notas: lista_decimal) retorna decimal
  retornar notas[longitud(notas) - 1]
fin_funcion

funcion estadoFinal(promedio: decimal) retorna texto
  si promedio >= 9 entonces
    retornar "Excelente"
  si_no
    si promedio >= 7 entonces
      retornar "Aprobado"
    si_no
      retornar "En riesgo"
    fin_si
  fin_si
fin_funcion

inicio
  definir notas como lista_decimal
  definir nota1 como decimal
  definir nota2 como decimal
  definir nota3 como decimal
  definir promedio como decimal

  notas = [0, 0, 0]

  leer nota1
  leer nota2
  leer nota3

  notas[0] = nota1
  notas[1] = nota2
  notas[2] = nota3

  promedio = promedioNotas(notas)

  mostrar "Notas capturadas: " + notas
  mostrar "Cantidad de notas: " + longitud(notas)
  mostrar "Ultima nota: " + ultimaNota(notas)
  mostrar "Promedio: " + promedio
  mostrar "Estado final: " + estadoFinal(promedio)
fin
```
