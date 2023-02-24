# Bandit Level 20 al Level 21

## Objetivo
There is a setuid binary in the homedirectory that does the following: it makes a connection to localhost on the port you specify as a commandline argument. It then reads a line of text from the connection and compares it to the password in the previous level (bandit20). If the password is correct, it will transmit the password for the next level (bandit21).

## Datos de acceso
bandit20
VxCazJaVykI6W36BkBU0mJTCM8rR95XT

## Solución
```bash
bandit20@bandit:~$ nc -nlvp 8765 <<< VxCazJaVykI6W36BkBU0mJTCM8rR95XT &
[4] 3123078
bandit20@bandit:~$ Listening on 0.0.0.0 8765

bandit20@bandit:~$ ./suconnect 8765
Connection received on 127.0.0.1 60840
Read: VxCazJaVykI6W36BkBU0mJTCM8rR95XT
Password matches, sending next password
NvEJF7oVjkddltPSrdKEFOllh9V1IBcq
bandit20@bandit:~$ fg
nc -nlvp 8765 <<< VxCazJaVykI6W36BkBU0mJTCM8rR95XT
^C
```

## Notas adicionales
| comando | descripción |
| ------ | ------ |
| xx | xx |

## Referencias
- []()