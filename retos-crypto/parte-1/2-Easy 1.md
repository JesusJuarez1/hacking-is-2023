# Easy 1

# Objetivo
The one time pad can be cryptographically secure, but not when you know the key. Can you solve this? We've given you the encrypted flag, key, and a table to help `UFJKXQZQUNB` with the key of `SOLVECRYPTO`. Can you use this [table](https://jupiter.challenges.picoctf.org/static/1fd21547c154c678d2dab145c29f1d79/table.txt) to solve it?.

# Pistas
- Submit your answer in our flag format. For example, if your answer was 'hello', you would submit 'picoCTF{HELLO}' as the flag.
- Please use all caps for the message.

# Solución
- Descargamos la tabla que nos prrporciona
- Abrimos la tabla
- Utilizamos [cyberchef](https://gchq.github.io/CyberChef/#recipe=Vigen%C3%A8re_Decode('SOLVECRYPTO')&input=VUZKS1hRWlFVTkI) con el filtro de "Vigenere Decode"
- Le proporcionamos el texto cifrado y la llave y obtenemos la bandera

# Bandera
picoCTF{CRYPTOISFUN}

## Notas adicionales
| comando | descripción |
| ------ | ------ |
| xx | xx |

## Referencias
- []()