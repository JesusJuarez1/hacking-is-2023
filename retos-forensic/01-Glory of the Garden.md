# Nombre

# Objetivo
This [garden](https://jupiter.challenges.picoctf.org/static/4153422e18d40363e7ffc7e15a108683/garden.jpg) contains more than it seems.

# Pistas
- What is a hex editor?

# Solución
```
┌──(kali㉿kali)-[~/picoctf/forensic/gloryofthegarden]
└─$ wget https://jupiter.challenges.picoctf.org/static/4153422e18d40363e7ffc7e15a108683/garden.jpg
--2023-03-23 14:19:01--  https://jupiter.challenges.picoctf.org/static/4153422e18d40363e7ffc7e15a108683/garden.jpg
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 2295192 (2.2M) [application/octet-stream]
Saving to: ‘garden.jpg’

garden.jpg          100%[================>]   2.19M  1.57MB/s    in 1.4s    

2023-03-23 14:19:03 (1.57 MB/s) - ‘garden.jpg’ saved [2295192/2295192]

                                                                             
┌──(kali㉿kali)-[~/picoctf/forensic/gloryofthegarden]
└─$ strings garden.jpg | grep "picoCTF"
Here is a flag "picoCTF{more_than_m33ts_the_3y33dd2eEF5}"
                                                                             
┌──(kali㉿kali)-[~/picoctf/forensic/gloryofthegarden]
└─$ 

```

# Bandera
picoCTF{more_than_m33ts_the_3y33dd2eEF5}

## Notas adicionales
| comando | descripción |
| ------ | ------ |
| xx | xx |

## Referencias
- []()