# asm1

# Objetivo
What does asm1(0x8be) return? Submit the flag as a hexadecimal value (starting with '0x'). NOTE: Your submission for this question will NOT be in the normal flag format. [Source](https://jupiter.challenges.picoctf.org/static/66c927e32f3d7be7a62d13a7c2250943/test.S)

# Pistas
- assembly [conditions](https://www.tutorialspoint.com/assembly_programming/assembly_conditions.htm)

# Solución
- Descargamos el archivo
- Analisamos el contenido del archivo
- Modificamos el archivo para simular la ejecución
```
stack

0000

[ ebp ] <-esp <-ebp
[ ret ] <- ebp + 0x4
[0x8be] <- ebp + 0x8
fffff  

registers    
[ 0x8bb ] eax

asm1:  
        <+0>:   push   ebp   
        <+1>:   mov    ebp,esp
        <+3>:   cmp    DWORD PTR [ebp+0x8],0x71c
        <+10>:  jg     0x512 <asm1+37>
        <+12>:  cmp    DWORD PTR [ebp+0x8],0x6cf
        <+19>:  jne    0x50a <asm1+29>
        <+21>:  mov    eax,DWORD PTR [ebp+0x8]
        <+24>:  add    eax,0x3
        <+27>:  jmp    0x529 <asm1+60>
        <+29>:  mov    eax,DWORD PTR [ebp+0x8]
        <+32>:  sub    eax,0x3
        <+35>:  jmp    0x529 <asm1+60>
        <+37>:  cmp    DWORD PTR [ebp+0x8],0x8be
        <+44>:  jne    0x523 <asm1+54>
        <+46>:  mov    eax,DWORD PTR [ebp+0x8]
        <+49>:  sub    eax,0x3
        <+52>:  jmp    0x529 <asm1+60>
        <+54>:  mov    eax,DWORD PTR [ebp+0x8]
        <+57>:  add    eax,0x3
        <+60>:  pop    ebp
        <+61>:  ret 
```

```
┌──(kali㉿kali)-[~]
└─$ python           
Python 3.10.8 (main, Nov  4 2022, 09:21:25) [GCC 12.2.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> 0x71c
1820
>>> 0x71c > 0x8be
False
>>> 0x8be > 0x71c
True
>>> 0x8be > 0x8be
False
>>> hex(0x8be-0x3)
'0x8bb'
```

# Bandera
0x8bb

## Notas adicionales
| comando | descripción |
| ------ | ------ |
| xx | xx |

## Referencias
- []()