# Bit-O-Asm-2

# Objetivo
Can you figure out what is in the `eax` register? Put your answer in the picoCTF flag format: `picoCTF{n}` where `n` is the contents of the `eax` register in the decimal number base. If the answer was `0x11` your flag would be `picoCTF{17}`. Download the assembly dump [here](https://artifacts.picoctf.net/c/510/disassembler-dump0_b.txt).

# Pistas
- `PTR`'s or 'pointers', reference a location in memory where values can be stored.

# Solución
- Descargamos el archivo
- Le hacemos un cat
- Inspeccionamos el codiigo
- Vemos que se hacen varias asignaciones
- en donde se termina asignando 0x9fe1a a eax
- Por lo tanto este es el valor que queremos
- Ya solo lo convertimos a ascii
```
┌──(kali㉿kali)-[~/picoctf/tercer-parcial/reverse/bitasm2]
└─$ cat disassembler-dump0_b.txt 
<+0>:     endbr64 
<+4>:     push   rbp
<+5>:     mov    rbp,rsp
<+8>:     mov    DWORD PTR [rbp-0x14],edi
<+11>:    mov    QWORD PTR [rbp-0x20],rsi
<+15>:    mov    DWORD PTR [rbp-0x4],0x9fe1a
<+22>:    mov    eax,DWORD PTR [rbp-0x4]
<+25>:    pop    rbp
<+26>:    ret
                                                                                                                                                                      
┌──(kali㉿kali)-[~/picoctf/tercer-parcial/reverse/bitasm2]
└─$ python
Python 3.10.8 (main, Nov  4 2022, 09:21:25) [GCC 12.2.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> ascii(0x9fe1a)
'654874'
>>> exit()
                                                                                                                                                                      
┌──(kali㉿kali)-[~/picoctf/tercer-parcial/reverse/bitasm2]
└─$ 

```

# Bandera
picoCTF{654874}

## Notas adicionales
| comando | descripción |
| ------ | ------ |
| xx | xx |

## Referencias
- []()