# Julie

`Julie` es la extension de almacenamiento de Thorio.

Sirve para guardar informacion en archivos y trabajar con SQLite.

## Que agrega Julie

- `guardar_texto(...)`
- `leer_texto(...)`
- `guardar_lineas(...)`
- `crear_directorio(...)`
- `sqlite_ejecutar(...)`
- `sqlite_consultar_texto(...)`
- `sqlite_consultar_filas(...)`

## Cuando conviene usarla

Julie es util cuando quieres que un programa:

- guarde notas o reportes
- cree carpetas de trabajo
- conserve datos entre ejecuciones
- haga consultas sencillas con SQLite

## Ejemplo con archivo

```thorio
inicio
  definir ruta como texto
  definir escrito como texto
  definir contenido como texto

  ruta = "examples/julie/sandbox/nota.txt"

  escrito = guardar_texto(ruta, "Julie guarda texto simple")
  contenido = leer_texto(ruta)

  mostrar "Archivo creado: " + escrito
  mostrar "Contenido leido: " + contenido
fin
```

## Ejemplo con SQLite

```thorio
inicio
  definir base como texto
  definir cambios como entero
  definir personas como lista_texto

  base = "examples/julie/sandbox/agenda.sqlite"

  cambios = sqlite_ejecutar(base, "create table if not exists agenda(nombre text)")
  cambios = sqlite_ejecutar(base, "delete from agenda")
  cambios = sqlite_ejecutar(base, "insert into agenda(nombre) values ('Ana')")
  cambios = sqlite_ejecutar(base, "insert into agenda(nombre) values ('Luis')")

  personas = sqlite_consultar_texto(base, "select nombre from agenda order by nombre")
  mostrar "Cantidad: " + longitud(personas)
  mostrar "Lista: " + personas
fin
```

## Flujo de persistencia

```mermaid
flowchart LR
    A["Datos del programa"] --> B["Guardar en archivo o SQLite"]
    B --> C["Volver a leer"]
    C --> D["Usar resultados"]
```

## Idea pedagogica

Julie ayuda a entender que un programa no siempre termina cuando acaba la ejecucion. A veces necesita dejar informacion guardada para usarla despues.

## Ejemplos relacionados

- [Guardar y leer texto](../../examples/julie/guardar-y-leer-texto.md)
- [Agenda SQLite](../../examples/julie/agenda-sqlite.md)

## Siguiente paso

Continua con [Thorio + Camile + Julie](./thorio-platform.md).
