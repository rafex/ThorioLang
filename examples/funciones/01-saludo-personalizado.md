---
runtime: thorio
uses:
  - thorio
ide_web_runnable: true
ide_web_reason: "Usa solo el lenguaje base y puede ejecutarse en el IDE web."
---

# Saludo personalizado

Crea una funcion que devuelve un saludo.

```thorio
funcion saludar(nombre: texto) retorna texto
  retornar "Hola " + nombre
fin_funcion

inicio
  mostrar saludar("Lucia")
fin
```
