---
runtime: thorio
uses:
  - thorio
ide_web_runnable: true
ide_web_reason: "Usa solo el lenguaje base y puede ejecutarse en el IDE web."
---

# Comparacion de usuarios

Compara textos con igualdad.

```thorio
inicio
  definir usuario como texto

  usuario = "admin"

  si usuario == "admin" entonces
    mostrar "Perfil de administracion"
  si_no
    mostrar "Perfil estandar"
  fin_si
fin
```
