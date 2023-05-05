# Lookey here

## Descripción
Attackers have hidden information in a very large mass of data in the past, maybe they are still doing it. Download the data [here](https://artifacts.picoctf.net/c/125/anthem.flag.txt).

## Pistas
- Download the file and search for the flag based on the known prefix.

## Solución
- Descargamos el archivo
- Le hacemos un cat junto a un grep
```bash
┌──(kali㉿kali)-[~/picoctf/forensic/lookeyhere]
└─$ cat anthem.flag.txt | grep "pico"
      we think that the men of picoCTF{gr3p_15_@w3s0m3_58f5c024}
```

## Bandera
picoCTF{gr3p_15_@w3s0m3_58f5c024}

## Notas adicionales
| comando | descripción |
| ------ | ------ |
| xx | xx |

## Referencias
- []()