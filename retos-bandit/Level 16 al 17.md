
# Bandit Level 15 al Level 17

## Objetivo
The credentials for the next level can be retrieved by submitting the password of the current level to **a port on localhost in the range 31000 to 32000**. First find out which of these ports have a server listening on them. Then find out which of those speak SSL and which don’t. There is only 1 server that will give the next credentials, the others will simply send back to you whatever you send to it.

## Datos de acceso
bandit16
JQttfApK4SeyHwDlI9SXGR50qclOAil1

## Solución
```bash
bandit16@bandit:~$ openssl s_client --connect localhost:31790

jesus@CHUY:~$ chmod 600 llave2.txt
jesus@CHUY:~$ ssh -i llave2.txt bandit17@bandit.labs.overthewire.org -p2220
bandit17@bandit:~$ cat /etc/bandit_pass/bandit17
VwOSWtCA7lRKkTfbr2IDh6awj9RNZM5e
```

## Notas adicionales
| comando | descripción |
| ------ | ------ |
| nmap localchost | Nos permite escanear los puestos de nuestra propia maquina |
| -p | Nos permite definir un rango de puertos |
| openssl | Nos permite conectar con un puerto |

## Referencias
- [Port Scanner](https://en.wikipedia.org/wiki/Port_scanner)