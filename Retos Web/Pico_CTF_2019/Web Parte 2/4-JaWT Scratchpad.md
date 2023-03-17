# JaWT Scratchpad

# Objetivo
Check the admin scratchpad! `https://jupiter.challenges.picoctf.org/problem/61864/` or http://jupiter.challenges.picoctf.org:61864

# Pistas
- What is that cookie?
- Have you heard of JWT?

# Solución
- Ingresamos a la pagina con cualquier usuario que no sea admin
- Obtenemos el jwt en las cookie
- Obtenemos la contraseña en kali
- ```
```┌──(kali㉿kali)-[~]
└─$ john token -w=/usr/share/wordlists/rockyou.txt
Using default input encoding: UTF-8
Loaded 1 password hash (HMAC-SHA256 [password is key, SHA256 128/128 SSE2 4x])
Will run 2 OpenMP threads
Press 'q' or Ctrl-C to abort, almost any other key for status
ilovepico        (?)     
1g 0:00:00:05 DONE (2023-03-14 15:00) 0.1766g/s 1306Kp/s 1306Kc/s 1306KC/s iloverob4live345..ilovepatri
Use the "--show" option to display all of the cracked passwords reliably
Session completed. 
```
- Cambiamos el jwt en la pagina https://jwt.io/, cambiando el usuario y agregando la contraseña
- Cambiamos la cookie de la pagina por la nueva y nos da la contraseña

# Bandera
picoCTF{jawt_was_just_what_you_thought_1ca14548}

## Notas adicionales
| comando | descripción |
| ------ | ------ |
| xx | xx |

## Referencias
- []()