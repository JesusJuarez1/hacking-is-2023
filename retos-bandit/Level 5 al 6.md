
# Bandit Level 5 al Level 6

## Objetivo
The password for the next level is stored in a file somewhere under the **inhere** directory and has all of the following properties:
-   human-readable
-   1033 bytes in size
-   not executable

## Datos de acceso
bandit5
lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR

## Solución
```bash
bandit5@bandit:~$ ls
inhere
bandit5@bandit:~$ cd inhere/
bandit5@bandit:~/inhere$ ls
maybehere00  maybehere03  maybehere06  maybehere09  maybehere12  maybehere15  maybehere18
maybehere01  maybehere04  maybehere07  maybehere10  maybehere13  maybehere16  maybehere19
maybehere02  maybehere05  maybehere08  maybehere11  maybehere14  maybehere17
bandit5@bandit:~/inhere$ find -readable -size 1033c -type f
./maybehere07/.file2
bandit5@bandit:~/inhere$ cat ./maybehere07/.file2
P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU
```

## Notas adicionales
| comando | descripción |
| ------ | ------ |
| find | Busca archivos por parametros |
| -readable | Busca archivos que sean legibles |
| -size | Busca por tamaño indicado |
| -type | Busca por tipo de archivo |

## Referencias
- [Buscar archivos por parametros](https://ed.team/blog/como-buscar-archivos-en-linux)
