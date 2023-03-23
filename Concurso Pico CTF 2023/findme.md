# rotation

# Objetivo
You will find the flag after decrypting this fileDownload the encrypted flag [here](https://artifacts.picoctf.net/c/391/encrypted.txt).

# Pistas
- Sometimes rotation is right

# Solución
- Con la pista sabemos que la bandera esta desplazada un numero indicado de posiciones en el abecedario, por lo que averiguamos por cuantas posiciones esta rotado y ejecutamos el sigueinte comando
```bash
jesjua-picoctf@webshell:~$ cat encrypted.txt | tr [a-zA-Z] [s-za-rS-ZA-R]
picoCTF{r0tat1on_d3crypt3d_7d140864}
jesjua-picoctf@webshell:~$ 
```

# Bandera
picoCTF{r0tat1on_d3crypt3d_7d140864}

## Notas adicionales
| comando | descripción |
| ------ | ------ |
| xx | xx |

## Referencias
- []()