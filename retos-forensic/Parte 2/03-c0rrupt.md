# c0rrupt

# Objetivo
We found this [file](https://jupiter.challenges.picoctf.org/static/ab30fcb7d47364b4190a7d3d40edb551/mystery). Recover the flag.

# Pistas
- Try fixing the file header

# Solución
- Descargamos el archivo
- La pista nos dice que el encabezado esta dañado
- con el comando hexaeditor lo reparamos para que quede de la siguiente forma
```
00000000: 8950 4e47 0d0a 1a0a 0000 000d 4948 4452  .PNG........IHDR
```
- Con esto el archivo ya sale en formato de imagen
```
┌──(kali㉿kali)-[~/picoctf/forensic/c0rrupt]
└─$ file mystery     
mystery: PNG image data, 1642 x 1095, 8-bit/color RGB, non-interlaced
```
- Aun asi no podemos ver la imagen debido a que aun esta dañada
- Para resolver esto instalamos la herramienta pngcheck
- Al ejecutar esta herramienta nos da el siguiente resultado
```
┌──(kali㉿kali)-[~/picoctf/forensic/c0rrupt]
└─$ pngcheck -v mystery 
zlib warning:  different version (expected 1.2.13, using 1.2.11)

File: mystery (202940 bytes)
  chunk IHDR at offset 0x0000c, length 13
    1642 x 1095 image, 24-bit RGB, non-interlaced
  chunk sRGB at offset 0x00025, length 1
    rendering intent = perceptual
  chunk gAMA at offset 0x00032, length 4: 0.45455
  chunk pHYs at offset 0x00042, length 9: 2852132389x5669 pixels/meter
  CRC error in chunk pHYs (computed 38d82c82, expected 495224f0)
ERRORS DETECTED in mystery
                                                                             
┌──(kali㉿kali)-[~/picoctf/forensic/c0rrupt]
└─$ 
```
- Lo cual nos dice que el chunk pHYs esta dañado
- Corregimos el chunk pHYs y el chunk IDTa para que queden de la siguiente manera
```00000040  00 09 70 48  59 73 00 00   16 25 00 00  16 25 01 49 .pHYs...%...%.I
00000050  52 24 F0 00  00 FF A5 49   44 41 54 78  5E EC BD 3F $.....IDATx^..? 
```
- Con esto el archivo no tiene errores y lo podemos abrir y ver la bandera

# Bandera
picoCTF{c0rrupt10n_1847995}

## Notas adicionales
| comando | descripción |
| ------ | ------ |
| xx | xx |

## Referencias
- []()