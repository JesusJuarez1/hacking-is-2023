
# Bandit Level 1 al Level 2

## Objetivo
The password for the next level is stored in a file called **-** located in the home directory

## Datos de acceso
bandit1
NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL

## Solución
```bash
bandit1@bandit:~$ ls
-
bandit1@bandit:~$ cat -
^C
bandit1@bandit:~$ cat ./-
rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi
```

## Notas adicionales

## Referencias
- [Archivos con guion](https://stackoverflow.com/questions/42187323/how-to-open-a-dashed-filename-using-terminal)