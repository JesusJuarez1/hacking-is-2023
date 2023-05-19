# Bit-O-Asm-3

# Objetivo
Can you figure out what is in the `eax` register? Put your answer in the picoCTF flag format: `picoCTF{n}` where `n` is the contents of the `eax` register in the decimal number base. If the answer was `0x11` your flag would be `picoCTF{17}`. Download the assembly dump [here](https://artifacts.picoctf.net/c/530/disassembler-dump0_c.txt).

# Pistas
- Not everything in this disassembly listing is optimal.

# Solución
- Descargamos el archivo
- Le hacemos un cat
- Inspeccionamos el codigo
- hacemos la ejecucion manual
- En esta ejecución nos da un valor al cual le tenemos que multiplicar otro
- Y al final tenemos que sumarle otro numero
- Y con esto obtenemos la bandera
```
┌──(kali㉿kali)-[~/picoctf/tercer-parcial/reverse/bitasm2]
└─$ cat disassembler-dump0_c.txt 
<+0>:     endbr64 
<+4>:     push   rbp
<+5>:     mov    rbp,rsp
<+8>:     mov    DWORD PTR [rbp-0x14],edi
<+11>:    mov    QWORD PTR [rbp-0x20],rsi
<+15>:    mov    DWORD PTR [rbp-0xc],0x9fe1a
<+22>:    mov    DWORD PTR [rbp-0x8],0x4
<+29>:    mov    eax,DWORD PTR [rbp-0xc]
<+32>:    imul   eax,DWORD PTR [rbp-0x8]
<+36>:    add    eax,0x1f5
<+41>:    mov    DWORD PTR [rbp-0x4],eax
<+44>:    mov    eax,DWORD PTR [rbp-0x4]
<+47>:    pop    rbp
<+48>:    ret
                                                                                                                                                                      
┌──(kali㉿kali)-[~/picoctf/tercer-parcial/reverse/bitasm2]
└─$ python
Python 3.10.8 (main, Nov  4 2022, 09:21:25) [GCC 12.2.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> ascii(0x9fe1a)
'654874'
>>> ascii(0x4)
'4'
>>> 654874 * 4
2619496
>>> ascii(0x1f5)
'501'
>>> 2619496 + 501
2619997
>>> 
```

# Bandera
picoCTF{2619997}

## Notas adicionales
| comando | descripción |
| ------ | ------ |
| xx | xx |

## Referencias
- []()