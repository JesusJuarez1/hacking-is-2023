
# Bandit Level 4 al Level 5

## Objetivo
The password for the next level is stored in the only human-readable file in the **inhere** directory. Tip: if your terminal is messed up, try the “reset” command.

## Datos de acceso
bandit4
2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe

## Solución
```bash
bandit4@bandit:~$ ls
inhere
bandit4@bandit:~$ cd inhere/
bandit4@bandit:~/inhere$ file ./*
./-file00: data
./-file01: data
./-file02: data
./-file03: data
./-file04: data
./-file05: data
./-file06: data
./-file07: ASCII text
./-file08: data
./-file09: data
bandit4@bandit:~/inhere$ cat ./-file07
lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR
```

## Notas adicionales
| comando | descripción |
| ------ | ------ |
| file | Muestra los tipos de archivo |

## Referencias
- []()