# Panel de repaso persistente

Integra funciones, Camile y Julie para construir una mini rutina persistente.

```thorio
funcion mensaje_de_repaso(tema: texto) retorna texto
  retornar "Tema sugerido para repaso: " + tema
fin_funcion

inicio
  definir tema como texto
  definir ruta como texto
  definir lineas como lista_texto

  tema = pedir_texto("Que tema quieres repasar esta tarde?")
  ruta = "examples/platform/sandbox/repaso.md"

  guardar_lineas(ruta, ["Repaso activo", mensaje_de_repaso(tema), "Estado: pendiente"])
  lineas = leer_lineas(ruta)

  mostrar_mensaje(lineas[0])
  mostrar_mensaje(lineas[1])
  mostrar_mensaje("Lineas guardadas: " + longitud(lineas))
fin
```
