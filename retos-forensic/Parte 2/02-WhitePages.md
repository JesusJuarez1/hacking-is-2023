# WhitePages

# Objetivo
I stopped using YellowPages and moved onto WhitePages... but [the page they gave me](https://jupiter.challenges.picoctf.org/static/95be9526e162185c741259a75dffa0ab/whitepages.txt) is all blank!

# Pistas


# Solución
- Descargamos el archivo
- El archivo es un txt pero al hacerle un cat todo lo que muestra es un espacio vacio
- Con el comando xxd identificamos el patrón que tiene el archivo en hexadecimal
- Descargamos la herramienta de pwntool de python para ayudarnos
- Luego escribimos este codigo en python con el cual nos ayudaremos para decodificar el archivo
```
from pwn import *

file = open('whitepages.txt', 'rb')
data = bytearray(file.read())
data = data.replace(b'\xe2\x80\x83',b'0')
data = data.replace(b'\x20',b'1')
data = data.decode('ascii')
data = unbits(data)

print(data)
```
- Ejecutando este codigo obtenemos la bandera
# Bandera
picoCTF{not_all_spaces_are_created_equal_7100860b0fa779a5bd8ce29f24f586dc}

## Notas adicionales
| comando | descripción |
| ------ | ------ |
| xx | xx |

## Referencias
- []()