# Sintaxis basica

Esta pagina resume algunas estructuras iniciales de Thorio.

## Programa minimo

```thorio
inicio
  mostrar "Hola"
fin
```

## Variables

```thorio
inicio
  definir nombre como texto
  definir edad como entero

  nombre = "Ana"
  edad = 12
fin
```

## Decision

```thorio
si edad >= 18 entonces
  mostrar "Mayor de edad"
si_no
  mostrar "Menor de edad"
fin_si
```

## Ciclo

```thorio
mientras contador <= 5 hacer
  mostrar contador
  contador = contador + 1
fin_mientras
```

## Funcion

```thorio
funcion doble(valor: entero) retorna entero
  retornar valor * 2
fin_funcion
```

## Lista

```thorio
inicio
  definir numeros como lista_entero

  numeros = [4, 8, 15, 16]
  mostrar numeros[0]
fin
```
