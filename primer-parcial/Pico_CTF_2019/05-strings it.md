# strings it

## Descripción
Can you find the flag in [file](https://jupiter.challenges.picoctf.org/static/fae9ac5267cd6e44124e559b901df177/strings) without running it?

## Pistas
- [strings](https://linux.die.net/man/1/strings)

## Solución
```bash
jesjua-picoctf@webshell:~$ chmod 777 strings 
jesjua-picoctf@webshell:~$ ./strings
Maybe try the 'strings' function? Take a look at the man page
jesjua-picoctf@webshell:~$ strings strings | grep pico
picoCTF{5tRIng5_1T_7f766a23}
jesjua-picoctf@webshell:~$ 
```

## Bandera
picoCTF{5tRIng5_1T_7f766a23}

## Notas adicionales
| comando | descripción |
| ------ | ------ |
| xx | xx |

## Referencias
- []()