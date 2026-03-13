---
runtime: thorio
uses:
  - thorio
ide_web_runnable: true
ide_web_reason: "Usa solo el lenguaje base y puede ejecutarse en el IDE web."
---

# Busqueda manual

Busca un valor dentro de una lista de texto.

```thorio
funcion contiene(valores: lista_texto, buscado: texto) retorna logico
  definir indice como entero

  indice = 0

  mientras indice < longitud(valores) hacer
    si valores[indice] == buscado entonces
      retornar verdadero
    si_no
      indice = indice + 1
    fin_si
  fin_mientras

  retornar falso
fin_funcion

inicio
  definir nombres como lista_texto

  nombres = ["Ana", "Luis", "Marta"]

  mostrar "Existe Luis: " + contiene(nombres, "Luis")
fin
```
