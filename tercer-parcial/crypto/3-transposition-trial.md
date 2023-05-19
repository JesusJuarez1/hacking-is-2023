# transposition-trial

# Objetivo
Our data got corrupted on the way here. Luckily, nothing got replaced, but every block of 3 got scrambled around! The first word seems to be three letters long, maybe you can use that to recover the rest of the message.Download the corrupted message [here](https://artifacts.picoctf.net/c/192/message.txt).

# Pistas
- Split the message up into blocks of 3 and see how the first block is scrambled

# Solución
- Descargamos el mensaje
- Vemos el formato y evaluamos como resolverlo
- Nos dice que lo dividamos en bloques de 3
- Hacemos un script en python para hacerlo automaticamente
```                                                                         
flag_enc = "heTfl g as iicpCTo{7F4NRP051N5_16_35P3X51N3_V091B0AE}2"

flag = ""
for i in range(12, len(flag_enc),3):
    temp = flag_enc[i:i+3]
    flag += temp[2] + temp[0:2]

print(flag)
```
- Ejecutamos el programa
```
┌──(kali㉿kali)-[~/picoctf/tercer-parcial/crypto/transportation]
└─$ python exploit.py
picoCTF{7R4N5P051N6_15_3XP3N51V3_109AB02E}
                                                                                                                                                                       
┌──(kali㉿kali)-[~/picoctf/tercer-parcial/crypto/transportation]
└─$ 
```
# Bandera
picoCTF{7R4N5P051N6_15_3XP3N51V3_109AB02E}

## Notas adicionales
| comando | descripción |
| ------ | ------ |
| xx | xx |

## Referencias
- []()