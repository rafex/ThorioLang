---
runtime: julie
uses:
  - thorio
  - julie
ide_web_runnable: false
ide_web_reason: "Usa 'leer' y Julie; requiere entrada interactiva, por lo que no es apto para el IDE web actual."
---

# Ejemplo Julie 06 - Lineas y directorio

Este ejemplo crea un directorio, guarda una lista de lineas, la vuelve a leer y limpia el archivo al final.

```thorio
funcion unirLineas(valores: lista_texto) retorna texto
  definir indice como entero
  definir salida como texto

  indice = 0
  salida = ""

  mientras indice < longitud(valores) hacer
    si indice == 0 entonces
      salida = valores[indice]
    si_no
      salida = salida + " / " + valores[indice]
    fin_si
    indice = indice + 1
  fin_mientras

  retornar salida
fin_funcion

inicio
  definir carpeta como texto
  definir archivo como texto
  definir lineas como lista_texto
  definir leidas como lista_texto
  definir existeAntes como logico
  definir existeDespues como logico
  definir eliminado como logico

  carpeta = crear_directorio("examples/julie/sandbox/lineas")
  archivo = carpeta + "/agenda.md"
  lineas = ["Ana", "Luis", "Marta"]

  existeAntes = existe_archivo(archivo)
  mostrar "Existe antes: " + existeAntes

  guardar_lineas(archivo, lineas)
  leidas = leer_lineas(archivo)
  existeDespues = existe_archivo(archivo)

  mostrar "Carpeta: " + carpeta
  mostrar "Existe despues: " + existeDespues
  mostrar "Cantidad: " + longitud(leidas)
  mostrar "Contenido: " + unirLineas(leidas)

  eliminado = eliminar_archivo(archivo)
  mostrar "Eliminado: " + eliminado
fin
```
