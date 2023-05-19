# GDB baby step 1

# Objetivo
Can you figure out what is in the `eax` register at the end of the `main` function? Put your answer in the picoCTF flag format: `picoCTF{n}` where `n` is the contents of the `eax` register in the decimal number base. If the answer was `0x11` your flag would be `picoCTF{17}`. Disassemble [this](https://artifacts.picoctf.net/c/512/debugger0_a).

# Pistas
- gdb is a very good debugger to use for this problem and many others!
- `main` is actually a recognized symbol that can be used with gdb commands.

# Solución
- Descargamos el archivo
- Lo abrimos con gdb
- Lo inspeccionamos
- Buscamos la funcion main
- Ahi se ve que le asigna el valor de 0x86342 y por lo tanto esto es la bandera
- Ya solo lo convertimos y listo (549698)
![Imagen](./img/Capture.png)

# Bandera
picoCTF{549698}

## Notas adicionales
| comando | descripción |
| ------ | ------ |
| xx | xx |

## Referencias
- []()