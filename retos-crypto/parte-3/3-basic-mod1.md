# basic-mod1

# Objetivo
We found this weird message being passed around on the servers, we think we have a working decryption scheme.Download the message [here](https://artifacts.picoctf.net/c/129/message.txt).Take each number mod 37 and map it to the following character set: 0-25 is the alphabet (uppercase), 26-35 are the decimal digits, and 36 is an underscore.Wrap your decrypted message in the picoCTF flag format (i.e. `picoCTF{decrypted_message}`)

# Pistas
- Do you know what `mod 37` means?
- `mod 37` means modulo 37. It gives the remainder of a number after being divided by 37.

# Solución
- Descargamos el mensaje
- Realizamos el siguiente programa en python con el que desifraremos el mensaje
```
datos = open('message.txt').read().split()

flag = 'picoCTF{'
for i in datos:
        c = int(i)%37
        if c >= 0 and c <= 25:
                s = chr(c+65) 
        elif c>=26 and c<=35:
                s = chr(c+22)
        else:
                s = '_'
        flag += s
flag += '}'
print(flag)
```
- Al ejecutar este programa obtendremos la bandera

# Bandera
picoCTF{R0UND_N_R0UND_ADD17EC2}

## Notas adicionales
| comando | descripción |
| ------ | ------ |
| xx | xx |

## Referencias
- []()