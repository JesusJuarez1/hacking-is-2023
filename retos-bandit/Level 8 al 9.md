
# Bandit Level 8 al Level 9

## Objetivo
The password for the next level is stored in the file **data.txt** and is the only line of text that occurs only once

## Datos de acceso
bandit8
TESKZC0XvTetK0S9xNwm25STk5iWrBvP

## Solución
```bash
bandit8@bandit:~$ ls
data.txt
bandit8@bandit:~$ sort data.txt | uniq -u
EN632PlfYiZbn3PhVK3XOGSlNInNE00t
```

## Notas adicionales
| comando | descripción |
| ------ | ------ |
| sort | Ordena las lineas de un archivo |
| uniq -u | Obtiene el unico no repetido de una lista |

## Referencias
- []()