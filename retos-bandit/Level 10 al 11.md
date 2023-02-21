
# Bandit Level 10 al Level 11

## Objetivo
The password for the next level is stored in the file **data.txt**, which contains base64 encoded data

## Datos de acceso
bandit10
G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s

## Solución
```bash
bandit10@bandit:~$ ls
data.txt
bandit10@bandit:~$ cat data.txt | base64 -d
The password is 6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM
```

## Notas adicionales
| comando | descripción |
| ------ | ------ |
| base64 | Codifica un mensjae |
| base64 -d | Decodificamos un mensaje |

## Referencias
- []()