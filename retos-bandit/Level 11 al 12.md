
# Bandit Level 11 al Level 12

## Objetivo
The password for the next level is stored in the file **data.txt**, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions

## Datos de acceso
bandit11
6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM

## Solución
```bash
bandit11@bandit:~$ ls
data.txt
bandit11@bandit:~$ cat data.txt
Gur cnffjbeq vf WIAOOSFzMjXXBC0KoSKBbJ8puQm5lIEi
bandit11@bandit:~$ cat data.txt | tr [a-zA-Z] [n-za-mN-ZA-M]
The password is JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv
```

## Notas adicionales
| comando | descripción |
| ------ | ------ |
| tr | Indica como esta compuesto un conjunto |
| tr [[a-zA-Z]] [[n-za-mN-ZA-M]] | Rota las letras minusculas y mayusculas 13 posiciones |

## Referencias
- [Indicar el compuesto en un conjunto](https://es.wikipedia.org/wiki/Tr_(Unix)#:~:text=El%20comando%20tr%20permite%20al,a%20la%20hora%20de%20definirlos.)