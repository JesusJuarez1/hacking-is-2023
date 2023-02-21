
# Bandit Level X al Level

## Objetivo
The password for the next level can be retrieved by submitting the password of the current level to **port 30000 on localhost**.

## Datos de acceso
bandit14
fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq

## Solución
```bash
bandit14@bandit:~$ nc localhost 30000
fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq
Correct!
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt

^C
bandit14@bandit:~$
```

## Notas adicionales
| comando | descripción |
| ------ | ------ |
| nc | Me permite conectar a un host en un puerto en espesifico |

## Referencias
- []()