# Hola Camile

Ejemplo visual basico con ventanas de entrada, mensaje y confirmacion.

```thorio
inicio
  definir nombre como texto
  definir continuar como logico

  nombre = pedir_texto("¿Como te llamas?")
  mostrar_mensaje("Hola " + nombre)
  continuar = confirmar("¿Quieres continuar?")

  si continuar entonces
    mostrar_mensaje("Seguimos trabajando con Thorio y Camile")
  si_no
    mostrar_mensaje("Hasta luego " + nombre)
  fin_si
fin
```
