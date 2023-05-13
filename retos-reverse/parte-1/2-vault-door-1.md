# vault-door-1

# Objetivo
This vault uses some complicated arrays! I hope you can make sense of it, special agent. The source code for this vault is here: [VaultDoor1.java](https://jupiter.challenges.picoctf.org/static/87e103a8db01087de9ccf5a7a022ddf8/VaultDoor1.java)

# Pistas
- Look up the charAt() method online.

# Solución
- Descargamos el archivo
- Inspeccionamos el codigo
- Vemos que la bandera esta desordenada en la comparaciòn
- Copiamos esto para ordenarlos
- Editamos el archivo para que en cada linea existan 2 digitos para ordenarlos
```
┌──(kali㉿kali)-[~/picoctf/reverse/vault-door-1]
└─$ cat bandera | sort | awk '{print($3)}' | tr -d "'" | tr -d "\n"
d35cr4mbl3_tH3_cH4r4cT3r5_f6daf4;                                                                                  
┌──(kali㉿kali)-[~/picoctf/reverse/vault-door-1]
└─$ 
```
- Y con esto ya tendriamos la bandera

# Bandera
picoCTF{d35cr4mbl3_tH3_cH4r4cT3r5_f6daf4}

## Notas adicionales
| comando | descripción |
| ------ | ------ |
| xx | xx |

## Referencias
- []()