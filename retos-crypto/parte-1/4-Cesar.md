# Cesar

# Objetivo
Decrypt this [message](https://jupiter.challenges.picoctf.org/static/7d707a443e95054dc4cf30b1d9522ef0/ciphertext).

# Pistas
- caesar cipher [tutorial](https://learncryptography.com/classical-encryption/caesar-cipher)

# Solución
- Descargamos el archivo
- Vemos que al hacer un cat nos da la bandera con el contenido de la bandera cifrada
```
┌──(kali㉿kali)-[~/picoctf/crypto/Caesar]
└─$ cat ciphertext 
picoCTF{gvswwmrkxlivyfmgsrhnrisegl} 
```
- En la pagina de [CyberChef](https://gchq.github.io/CyberChef/#recipe=ROT13(true,true,false,22)&input=Z3Zzd3dtcmt4bGl2eWZtZ3NyaG5yaXNlZ2w) Buscamos el numero de rotación que se utilizo
- No damos cuenta que se roto 22 veces

# Bandera
picoCTF{crossingtherubicondjneoach}

## Notas adicionales
| comando | descripción |
| ------ | ------ |
| xx | xx |

## Referencias
- []()