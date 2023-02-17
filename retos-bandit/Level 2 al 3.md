
# Bandit Level 2 al 3

## Objetivo
The password for the next level is stored in a file called **spaces in this filename** located in the home directory

## Datos de acceso
bandit2
rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi

## Solución
```bash
bandit2@bandit:~$ ls
spaces in this filename
bandit2@bandit:~$ cat spaces in this filename
cat: spaces: No such file or directory
cat: in: No such file or directory
cat: this: No such file or directory
cat: filename: No such file or directory
bandit2@bandit:~$ cat spaces\ in\ this\ filename
aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG
```

## Notas adicionales
- Cuando hay espacios en el nombre hay que delimitarlo con "" o antes de un espacio poner un \

## Referencias
- [nombre de archivo con espacios](https://linuxhint.com/reference-filename-with-spaces-linux/)
