# asm2

# Objetivo
What does asm2(0xb,0x2e) return? Submit the flag as a hexadecimal value (starting with '0x'). NOTE: Your submission for this question will NOT be in the normal flag format. [Source](https://jupiter.challenges.picoctf.org/static/717467c8c8b4332ea5873ad8fe7b2dad/test.S)

# Pistas
- assembly [conditions](https://www.tutorialspoint.com/assembly_programming/assembly_conditions.htm)

# Solución
- Descargamos el archivo
- Lo analisamos es un archivo de lenguaje ensamblador 
- Abrimos el archivo para simular la ejecución del codigo
- No pude realizarlo porque tenia el problema de la linea asm2+24 que contiene un sub (el cual es una resta) pero no pude porque el numero 0xffffff80 ya no estaba en formato de 32 bits
- Acudi a una liga en internet el cual tenia el mismo problema que yo
- [asm2](https://dev.to/rooyca/picoctf-writeup-reverse-engineering-asm2-1659)
- Aqui la persona hizo un codigo en python el cual simula lo que hace el codigo ensamblador
```
 asm2:
	<+0>:	push   ebp
	<+1>:	mov    ebp,esp
	<+3>:	sub    esp,0x10
	<+6>:	mov    eax,DWORD PTR [ebp+0xc]
	<+9>:	mov    DWORD PTR [ebp-0x4],eax
	<+12>:	mov    eax,DWORD PTR [ebp+0x8]
	<+15>:	mov    DWORD PTR [ebp-0x8],eax
	<+18>:	jmp    0x509 <asm2+28>
	<+20>:	add    DWORD PTR [ebp-0x4],0x1
	<+24>:	sub    DWORD PTR [ebp-0x8],0xffffff80
	<+28>:	cmp    DWORD PTR [ebp-0x8],0x63f3
	<+35>:	jle    0x501 <asm2+20>
	<+37>:	mov    eax,DWORD PTR [ebp-0x4]
	<+40>:	leave  
	<+41>:	ret    

```
- **codigo**
```
'''
Stack:
[  local4 ]  <--- ebp-0x10
[  local3 ]  <--- ebp-0xc
[  local2 ]  <--- ebp-0x8
[  local1 ]  <--- ebp-0x4
[   ebp   ]
[   ret   ]  <--- ebp+0x4
[   arg1  ]  <--- ebp+0x8
[   arg2  ]  <--- ebp+0xc
'''
#We know that asm2 receives two arguments
def asm2(arg1, arg2):
#asm2:
    #<+0>:  push   ebp
    #<+1>:  mov    ebp,esp
    #<+3>:  sub    esp,0x10

    #<+6>:  mov    eax,DWORD PTR [ebp+0xc]
    eax = arg2

    #<+9>:  mov    DWORD PTR [ebp-0x4],eax
    local1 = eax

    #<+12>: mov    eax,DWORD PTR [ebp+0x8]
    eax = arg1

    #<+15>: mov    DWORD PTR [ebp-0x8],eax
    local2 = eax

    #<+18>: jmp    0x509 <asm2+28>
    #<+20>: add    DWORD PTR [ebp-0x4],0x1
    #<+24>: sub    DWORD PTR [ebp-0x8],0xffffff80
    #<+28>: cmp    DWORD PTR [ebp-0x8],0x63f3
    #<+35>: jle    0x501 <asm2+20>
    while(local2 <= 0x63f3):
        local1 = (local1 + 1) & 0xffffffff              #This truncates the result to 32 bits.
        local2 = (local2 - 0xffffff80)  & 0xffffffff    #This truncates the result to 32 bits.           
    '''
       It is necessary to truncate the restuls because in python does not have
       buffer overflow but 0x86 can have so we have to truncate it.
       '''

    #<+37>: mov    eax,DWORD PTR [ebp-0x4]
    #<+40>: leave
    #<+41>: ret
    return hex(local1)

print(asm2(0xb, 0x2e))
```
- Al ejecutar este codigo imprime la bandera
```
┌──(kali㉿kali)-[~/picoctf/reverse/asm2]
└─$ python exploit.py 
0xf6
```

# Bandera
0xf6

## Notas adicionales
| comando | descripción |
| ------ | ------ |
| xx | xx |

## Referencias
- []()