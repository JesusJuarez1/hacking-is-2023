# Matryoshka doll

# Objetivo
Matryoshka dolls are a set of wooden dolls of decreasing size placed one inside another. What's the final one? Image: [this](https://mercury.picoctf.net/static/1b70cffdd2f05427fff97d13c496963f/dolls.jpg)

# Pistas
- Wait, you can hide files inside files? But how do you find them?
- Make sure to submit the flag as picoCTF{XXXXX}

# Solución
- Descargamos el archivo
- La imagen es una matryoshka
- Con la herramienta "binwalk" podemos ver que tiene dentro el archivo
```
┌──(kali㉿kali)-[~/picoctf/forensic/Matryoshkadoll]
└─$ binwalk dolls.jpg 

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 594 x 1104, 8-bit/color RGBA, non-interlaced
3226          0xC9A           TIFF image data, big-endian, offset of first image directory: 8
272492        0x4286C         Zip archive data, at least v2.0 to extract, compressed size: 378954, uncompressed size: 383938, name: base_images/2_c.jpg
651612        0x9F15C         End of Zip archive, footer length: 22
```
- Nos damos cuenta que dentro contiene un archivo ZIP
- usamos binwalk para extraer el archivo
```
┌──(kali㉿kali)-[~/picoctf/forensic/Matryoshkadoll]
└─$ binwalk -e dolls.jpg 

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
d0             0x0             PNG image, 594 x 1104, 8-bit/color RGBA, non-interlaced
3226          0xC9A           TIFF image data, big-endian, offset of first image directory: 8
272492        0x4286C         Zip archive data, at least v2.0 to extract, compressed size: 378954, uncompressed size: 383938, name: base_images/2_c.jpg
651612        0x9F15C         End of Zip archive, footer length: 22

                                                                             
┌──(kali㉿kali)-[~/picoctf/forensic/Matryoshkadoll]
└─$ cd _dolls.jpg.extracted 
                                                                             
┌──(kali㉿kali)-[~/picoctf/forensic/Matryoshkadoll/_dolls.jpg.extracted]
└─$ ls
4286C.zip  base_images
                                                                             
┌──(kali㉿kali)-[~/picoctf/forensic/Matryoshkadoll/_dolls.jpg.extracted]
└─$ cd base_images         
                                                                             
┌──(kali㉿kali)-[~/…/forensic/Matryoshkadoll/_dolls.jpg.extracted/base_images]                                                                            
└─$ ls
2_c.jpg
                                                                             
┌──(kali㉿kali)-[~/…/forensic/Matryoshkadoll/_dolls.jpg.extracted/base_images]                                                                            
└─$ 
```
- Esta imagen sigue siendo una matryoshka
- Vamos a repetir el paso de extraer lo que tenga la imagen varias veces hasta obtener que no se pueda extraer mas
- Al final nos da un archivo llamado "flag.txt" al cual nadamas le hacemos un cat y ahí esta la bandera
```
┌──(kali㉿kali)-[~/…/base_images/_3_c.jpg.extracted/base_images/_4_c.jpg.extracted]
└─$ cat flag.txt                
picoCTF{bf6acf878dcbd752f4721e41b1b1b66b} 
```

# Bandera
picoCTF{bf6acf878dcbd752f4721e41b1b1b66b}

## Notas adicionales
| comando | descripción |
| ------ | ------ |
| xx | xx |

## Referencias
- []()