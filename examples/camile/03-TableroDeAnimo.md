# Tablero de animo

Muestra listas como texto y usa dialogos para elegir un estado inicial.

```thorio
inicio
  definir estados como lista_texto
  definir estado_actual como texto
  definir seguir como logico

  estados = ["enfoque", "pausa", "energia"]
  mostrar_mensaje("Estados disponibles: " + estados)
  estado_actual = pedir_texto("Con cual estado quieres empezar?")
  seguir = confirmar("Deseas registrar el estado " + estado_actual + "?")

  si seguir entonces
    mostrar_mensaje("Estado inicial guardado: " + estado_actual)
    mostrar_mensaje("Total de estados sugeridos: " + longitud(estados))
  si_no
    mostrar_mensaje("Se cancelo el registro inicial.")
  fin_si
fin
```
