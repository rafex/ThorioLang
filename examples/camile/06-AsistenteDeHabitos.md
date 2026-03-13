# Asistente de habitos

Ejemplo intermedio con varias confirmaciones y mensajes personalizados.

```thorio
inicio
  definir habito como texto
  definir hecho_hoy como logico
  definir repetir_manana como logico

  habito = pedir_texto("Que habito quieres revisar?")
  hecho_hoy = confirmar("Ya cumpliste " + habito + " hoy?")

  si hecho_hoy entonces
    repetir_manana = confirmar("Quieres repetir " + habito + " manana?")
    si repetir_manana entonces
      mostrar_mensaje("Excelente. Deja listo un recordatorio para manana.")
    si_no
      mostrar_mensaje("Buen trabajo. Hoy fue suficiente.")
    fin_si
  si_no
    mostrar_mensaje("Haz una version pequena del habito para no romper la racha.")
  fin_si
fin
```
