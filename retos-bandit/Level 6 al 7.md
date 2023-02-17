
# Bandit Level 6 al Level 7

## Objetivo
The password for the next level is stored **somewhere on the server** and has all of the following properties:
-   owned by user bandit7
-   owned by group bandit6
-   33 bytes in size

## Datos de acceso
bandit6
P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU

## Solución
```bash
bandit6@bandit:~$ find / -user bandit7 -group bandit6 -size 33c 2>/dev/null
/var/lib/dpkg/info/bandit7.password
bandit6@bandit:~$ cat /var/lib/dpkg/info/bandit7.password
z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S
```

## Notas adicionales
| comando | descripción |
| ------ | ------ |
| find -user | Busca por el usuario |
| find -group | Busca por grupo |
| 2>/dev/null | Manda todos los errores de un comando a null (no se muestran en la salida) |

## Referencias
- []()