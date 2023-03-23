# Reverse

# Objetivo
Try reversing this file? Can ya?I forgot the password to this [file](https://artifacts.picoctf.net/c/270/ret). Please find it for me?

# Pistas


# Solución
- Descargamos el archivo y lo tratamos de leer con cat lo que nos resulta en caracteres extraños
- Le aplicamos el siguinte comando con el cual formateamos el contenido del archivo a texto normal lo que nos da como resultado la bandera
- 
```
jesjua-picoctf@webshell:~$ strings ret | grep "picoCTF"
picoCTF{H
Password correct, please see flag: picoCTF{3lf_r3v3r5ing_succe55ful_c83965de}
jesjua-picoctf@webshell:~$
```


# Bandera
picoCTF{3lf_r3v3r5ing_succe55ful_c83965de}

## Notas adicionales
| comando | descripción |
| ------ | ------ |
| xx | xx |

## Referencias
- []()