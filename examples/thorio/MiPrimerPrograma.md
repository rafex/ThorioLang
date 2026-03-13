---
runtime: thorio
uses:
  - thorio
ide_web_runnable: true
ide_web_reason: "Usa solo el lenguaje base y puede ejecutarse en el IDE web."
---

# Mi Primer Programa

```thorio
inicio
  definir nombre como texto
  definir contador como entero
  definir otroNombre como texto

  nombre = "Pedro"
  otroNombre = "Juan" 
  contador = 1

  mostrar "Hola " + nombre

  mientras contador <= 3 hacer
    mostrar contador
    mostrar otroNombre
    contador = contador + 1
  fin_mientras
fin
```
