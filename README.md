# Taller Aliases Git

## Ejercicio 1:

> Esta trabajando en un proyecto Git colaborativo con varias ramas y commits. Tu tarea es
> utilizar el comando git log con algunas opciones específicas para obtener un resumen
> gráfico de los últimos 5 commits en todas las ramas.

```bash
git log --max-count=5
```

- `--max-count=5` **->** Limita el numero maximo de commits que se mostraran al ejecutarse 

## Ejercicio 2:

> Esta trabajando en un proyecto Git colaborativo y necesitas obtener una visión gráfica y
> detallada del historial de commits. Tu tarea es utilizar el comando git log con opciones
> específicas para personalizar el formato y presentación de la salida. La salida debe tener
> las siguientes especificaciones:
>
> - Muestra una representación gráfica del historial de commits
>
> - Muestra el hash corto del commit en color rojo
>
> - Muestra las referencias (ramas o tags) en las que está involucrado el commit en color
>   amarillo
>
> - Muestra el mensaje del commit.
>
> - Muestra la fecha relativa del commit en color verde.
>
> - Muestra el hash del commit como un identificador abreviado.
>
> - Muestra las fechas de los commits de forma relativa

```bash
git log --graph --abbrev-commit --decorate --pretty=format:'%C(red)%h %C(yellow)%d %C(white)%S %s %C(green)%ar'
```

## Ejercicio 3

>Estas trabajas frecuentemente con el comando git log -1 HEAD para obtener detalles sobre
>el último commit en la rama actual. Sin embargo, encuentras que escribir este comando
>completo es un poco tedioso. Quieres simplificarlo creando un alias personalizado.
>
>Tu tarea es utilizar el comando git config para crear un alias llamado last que represente el
>comando git log -1 HEAD.

```bash
git config --global alias.h1 "log -1 HEAD"
```

## Ejercicio 4

