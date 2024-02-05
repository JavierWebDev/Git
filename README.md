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

- `--graph` **->** Muestra una representacion rapida del historial de commits
- `--abbrev-commit` **->** Muestra unicamente la version abreviada del hash del commit
- `--decorate` **->** Muestra las ramas y tags junto a los commits
- `--pretty=format:'%C(red)%h %C(yellow)%d %C(white)%S %s %C(green)%ar'` **->**
  - `%C(red)`**->** Establece el color rojo para el siguiente texto.
  - `%h` **->** Muestra el hash corto del commit.
  - `%C(yellow)` **->** Establece el color amarillo para el siguiente texto.
  - `%d` **->** Muestra las referencias (ramas y tags)
  - `%C(white)` **->** Establece el color blanco para el siguiente texto
  - `%s`**->** Muestra el mensaje del commit
  - `%C(green)` **->** Establece el color verde para el siguiente texto
  - `%ar`**->** Muestra la fecha relativa del commit



## Ejercicio 3

>Estas trabajas frecuentemente con el comando git log -1 HEAD para obtener detalles sobre
>el último commit en la rama actual. Sin embargo, encuentras que escribir este comando
>completo es un poco tedioso. Quieres simplificarlo creando un alias personalizado.
>
>Tu tarea es utilizar el comando git config para crear un alias llamado last que represente el
>comando git log -1 HEAD.

```bash
git config --global alias.h1 "log -1 HEAD"
git h1
```

- `git config --global` **->** Establece la configuración global de git
- `alias.h1` **->** Crea un alias llamado `h1`
- `"log -1 HEAD"` **->**  Define el comando que se ejecutará cuando uses el alias `h1`



## Ejercicio 4

> Imagina que deseas simplificar el proceso de editar la configuración global de Git. Tu tarea
> es utilizar el comando git config para crear un alias que te permita abrir fácilmente la
> configuración global en tu editor de texto preferido. Ejecuta el comando para crear un alias
> llamado ec que cumpla con la especificación dada

```bash
git config --global alias.ec "config --global core.editor 'code -wait'"
git ec
```

`git config --global` **->** Establece la configuración a nivel global.

`alias.ec` **->** Crea un alias llamado `ec`.

`config --global core.editor 'code -wait"` **->** Configura el editor predeterminado como Visual Studio Code con la opción `-wait

## Ejercicio 5

> Imagina que estás trabajando en un proyecto Git colaborativo con múltiples colaboradores
> y ramas. Tu tarea es utilizar el comando git log con opciones específicas para personalizar
> la salida del historial de commits y resaltar información clave. El resultado de la ejecución
> del comando se debe ve como el ejemplo siguiente:

```bash
git log --graph --abbrev-commit --decorate --pretty=format:'%C(yellow) %h/ %C(red)/%d %C(white) %S %s %C(blue)/ %an'
```

- `--graph` **->** Muestra una representación gráfica del historial de commits.
- `--abbrev-commit` **->** Muestra un hash de commit abreviado.
- `--decorate` **->** Muestra las referencias (ramas y tags) en el historial.
- `--pretty=format` **->** Personaliza el formato de salida del historial de commits.
- `%C(yellow)` **->** Establece el color amarillo para el siguiente texto.
- `%h` **->** Muestra el hash corto del commit.
- `%C(red)` **->** Establece el color rojo para el siguiente texto.
- `%d` **->** Muestra las referencias (ramas y tags).
- `%C(white)` **->** Establece el color blanco para el siguiente texto.
- `%S` **->** Muestra el nombre del firmante del commit.
- `%s` **->** Muestra el mensaje del commit.
- `%C(blue)` **->** Establece el color azul para el siguiente texto.
- `%an` **->** Muestra el nombre del autor del commit.
