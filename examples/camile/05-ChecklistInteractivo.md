---
runtime: camile
uses:
  - thorio
  - camile
ide_web_runnable: false
ide_web_reason: "Usa Camile y requiere dialogos de escritorio, por lo que no es apto para el IDE web."
---

# Checklist interactivo

Usa listas e indexacion para mostrar una rutina guiada.

```thorio
funcion ultimo_paso(pasos: lista_texto) retorna texto
  retornar pasos[longitud(pasos) - 1]
fin_funcion

inicio
  definir pasos como lista_texto
  definir listo como logico

  pasos = ["leer teoria", "resolver ejemplo", "explicar resultado"]
  mostrar_mensaje("Plan del bloque: " + pasos)
  listo = confirmar("Ya completaste el primer paso?")

  si listo entonces
    mostrar_mensaje("Muy bien. El ultimo paso sera: " + ultimo_paso(pasos))
  si_no
    mostrar_mensaje("Empieza por el primer paso y vuelve a revisar tu avance.")
  fin_si
fin
```
