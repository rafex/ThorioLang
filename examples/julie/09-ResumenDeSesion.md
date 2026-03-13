# Resumen de sesion

Escribe una bitacora en Markdown, anexa mas texto y luego lee el resultado completo.

```thorio
inicio
  definir ruta como texto
  definir contenido como texto

  ruta = "examples/julie/sandbox/resumen_sesion.md"

  guardar_texto(ruta, "# Resumen\n")
  anexar_texto(ruta, "- Tema: Funciones y listas\n")
  anexar_texto(ruta, "- Estado: completado\n")

  contenido = leer_texto(ruta)

  mostrar "Existe archivo: " + existe_archivo(ruta)
  mostrar contenido
fin
```
