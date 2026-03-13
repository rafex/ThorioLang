---
runtime: camile
uses:
  - thorio
  - camile
ide_web_runnable: false
ide_web_reason: "Usa Camile y requiere dialogos de escritorio, por lo que no es apto para el IDE web."
---

# Ruta de estudio

Combina funciones, decisiones y mensajes visuales.

```thorio
funcion sugerencia_para(materia: texto) retorna texto
  si materia == "matematicas" entonces
    retornar "Empieza con ejercicios cortos y repite hasta dominar el patron."
  si_no
    retornar "Lee un ejemplo, despues explica con tus palabras lo aprendido."
  fin_si
fin_funcion

inicio
  definir materia como texto

  materia = pedir_texto("Que materia quieres estudiar hoy?")
  mostrar_mensaje("Ruta recomendada para " + materia)
  mostrar_mensaje(sugerencia_para(materia))
fin
```
