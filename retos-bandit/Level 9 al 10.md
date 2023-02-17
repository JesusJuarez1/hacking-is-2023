
# Bandit Level 9 al Level 10

## Objetivo
The password for the next level is stored in the file **data.txt** in one of the few human-readable strings, preceded by several ‘=’ characters.

## Datos de acceso
bandit9
EN632PlfYiZbn3PhVK3XOGSlNInNE00t

## Solución
```bash
bandit9@bandit:~$ ls
data.txt
bandit9@bandit:~$ strings data.txt | grep "=="
c========== the
h;========== password
========== isT
n.E========== G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s
```

## Notas adicionales
| comando | descripción |
| ------ | ------ |
| strings | Muestra las cadenas de un archivo |

## Referencias
- []()