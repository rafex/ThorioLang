# Serie de temperaturas

Ejemplo avanzado de listas, funciones, ciclos e indexacion.

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
  definir temperaturas como lista_decimal

  temperaturas = [21.5, 23.0, 24.5, 22.0]

  mostrar "Lecturas: " + temperaturas
  mostrar "Promedio: " + promedio(temperaturas)
fin
```
