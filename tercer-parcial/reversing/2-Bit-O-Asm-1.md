# Bit-O-Asm-1

# Objetivo
Can you figure out what is in the `eax` register? Put your answer in the picoCTF flag format: `picoCTF{n}` where `n` is the contents of the `eax` register in the decimal number base. If the answer was `0x11` your flag would be `picoCTF{17}`. Download the assembly dump [here](https://artifacts.picoctf.net/c/509/disassembler-dump0_a.txt).

# Pistas
- As with most assembly, there is a lot of noise in the instruction dump. Find the one line that pertains to this question and don't second guess yourself!

# Solución
- Descargamos el archivo
- Le hacemos un cat
- Vemos que son instrucciones de ensamblador
- Vemos que nos piden un numero hex y el unico número que se mueve es el 0x30 el cual corresponde al valor de 48
```
┌──(kali㉿kali)-[~/picoctf/tercer-parcial/reverse/asciiftw]
└─$ cat disassembler-dump0_a.txt      
<+0>:     endbr64 
<+4>:     push   rbp
<+5>:     mov    rbp,rsp
<+8>:     mov    DWORD PTR [rbp-0x4],edi
<+11>:    mov    QWORD PTR [rbp-0x10],rsi
<+15>:    mov    eax,0x30
<+20>:    pop    rbp
<+21>:    ret
                                                                                                                                                                      
┌──(kali㉿kali)-[~/picoctf/tercer-parcial/reverse/asciiftw]
└─$ python                      
Python 3.10.8 (main, Nov  4 2022, 09:21:25) [GCC 12.2.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> ascii(0x30)
'48'
>>> exit
Use exit() or Ctrl-D (i.e. EOF) to exit
>>> exit()
                                                                                                                                                                      
┌──(kali㉿kali)-[~/picoctf/tercer-parcial/reverse/asciiftw]
└─$ 

```

# Bandera
picoCTF{48}

## Notas adicionales
| comando | descripción |
| ------ | ------ |
| xx | xx |

## Referencias
- []()