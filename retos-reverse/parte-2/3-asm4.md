# asm4

# Objetivo
What will asm4("picoCTF_f97bb") return? Submit the flag as a hexadecimal value (starting with '0x'). NOTE: Your submission for this question will NOT be in the normal flag format. [Source](https://jupiter.challenges.picoctf.org/static/76ef117df9226a8a9306a8865b14068e/test.S)

# Pistas
- Treat the Array argument as a pointer

# Solución
- Descargamos el archivo
- Inspeccionamos el archivo
- Vemos que esta muy extenso como para simular la ejecución del codigo
- Por lo que le vamos a realizar algunos ajustes para poder ejecutarlo
- Creamos un archivo nuevo con el codigo ensamblador modificado
```
.intel_syntax noprefix
.global asm4
asm4:
        push   ebp
        mov    ebp,esp
        push   ebx
        sub    esp,0x10
        mov    DWORD PTR [ebp-0x10],0x27a
        mov    DWORD PTR [ebp-0xc],0x0
        jmp    asm4+27
        add    DWORD PTR [ebp-0xc],0x1
        mov    edx,DWORD PTR [ebp-0xc]
        mov    eax,DWORD PTR [ebp+0x8]
        add    eax,edx
        movzx  eax,BYTE PTR [eax]
        test   al,al
        jne    asm4+23
        mov    DWORD PTR [ebp-0x8],0x1
        jmp    asm4+138
        mov    edx,DWORD PTR [ebp-0x8]
        mov    eax,DWORD PTR [ebp+0x8]
        add    eax,edx
        movzx  eax,BYTE PTR [eax]
        movsx  edx,al
        mov    eax,DWORD PTR [ebp-0x8]
        lea    ecx,[eax-0x1]
        mov    eax,DWORD PTR [ebp+0x8]
        add    eax,ecx
        movzx  eax,BYTE PTR [eax]
        movsx  eax,al
        sub    edx,eax
```
- Hacemos un codigo en c el cual mande llamar la función del codigo ensambaldor asm4 con el parametro que nos indican
```
#include <stdio.h>

int main() {
        printf("flag: 0x%X\n", asm4("picoCTF_f97bb"));
}
```
- Por ultimo compilamos y ejecutamos los codigos uniendolos
```
┌──(kali㉿kali)-[~/picoctf/reverse/asm4]
└─$ ls
chal.s  solve.c  test.S
                                                                                  
┌──(kali㉿kali)-[~/picoctf/reverse/asm4]
└─$ gcc -m32 -c chal.s -o chal.o
                                                                                  
┌──(kali㉿kali)-[~/picoctf/reverse/asm4]
└─$ gcc -m32 -c solve.c -o solve.o -w
                                                                                  
┌──(kali㉿kali)-[~/picoctf/reverse/asm4]
└─$ gcc -m32 -o a.out solve.o chal.o 
/usr/bin/ld: warning: chal.o: missing .note.GNU-stack section implies executable stack
/usr/bin/ld: NOTE: This behaviour is deprecated and will be removed in a future version of the linker
                                                                                  
┌──(kali㉿kali)-[~/picoctf/reverse/asm4]
└─$ ls                              
a.out  chal.o  chal.s  solve.c  solve.o  test.S
                                                                                  
┌──(kali㉿kali)-[~/picoctf/reverse/asm4]
└─$ ./a.out                          
flag: 0x265
                                                                                  
┌──(kali㉿kali)-[~/picoctf/reverse/asm4]
└─$ 
```

# Bandera
0x265

## Notas adicionales
| comando | descripción |
| ------ | ------ |
| xx | xx |

## Referencias
- []()