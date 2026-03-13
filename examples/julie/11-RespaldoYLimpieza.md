---
runtime: julie
uses:
  - thorio
  - julie
ide_web_runnable: true
ide_web_reason: "Usa Julie y puede ejecutarse en el entorno temporal del IDE web."
---

# Respaldo y limpieza

Trabaja con directorios, existencia y eliminacion de archivos.

```thorio
inicio
  definir carpeta como texto
  definir archivo como texto

  carpeta = "examples/julie/sandbox/respaldo"
  archivo = carpeta + "/nota.md"

  crear_directorio(carpeta)
  guardar_texto(archivo, "# Nota\nRecordar revisar el reporte final.")

  mostrar "Archivo creado: " + existe_archivo(archivo)
  mostrar leer_texto(archivo)
  mostrar "Archivo eliminado: " + eliminar_archivo(archivo)
  mostrar "Archivo disponible despues: " + existe_archivo(archivo)
fin
```
