# plumbing

## Descripción
Sometimes you need to handle process data outside of a file. Can you find a way to keep the output from this program and search for the flag? Connect to `jupiter.challenges.picoctf.org 4427`.

## Pistas
- Remember the flag format is picoCTF{XXXX}
- What's a pipe? No not that kind of pipe... This [kind](http://www.linfo.org/pipes.html)

## Solución
```bash
jesjua-picoctf@webshell:~$ nc jupiter.challenges.picoctf.org 4427 | grep "picoCTF"
picoCTF{digital_plumb3r_5ea1fbd7}
```

## Bandera
picoCTF{digital_plumb3r_5ea1fbd7}

## Notas adicionales
| comando | descripción |
| ------ | ------ |
| xx | xx |

## Referencias
- []()