# The Numbers

# Objetivo
The [numbers](https://jupiter.challenges.picoctf.org/static/f209a32253affb6f547a585649ba4fda/the_numbers.png)... what do they mean?

# Pistas
- The flag is in the format PICOCTF{}

# Solución
- Descargamos el archivo
- Al abrir el archivo nos damos cuenta que tiene una serie de numeros los cuales estan en formato de la bandera pero no es la bandera
- Convertimos los numeros a letras en la pagina [cyberchef](https://gchq.github.io/CyberChef/#recipe=A1Z26_Cipher_Decode('Space')&input=MTYgOSAzIDE1IDMgMjAgNiB7IDIwIDggNSAxNCAyMSAxMyAyIDUgMTggMTkgMTMgMSAxOSAxNSAxNCB9) aplicando el filtr "A1Z26 Cipher Decode"
- Con esto obtenemos la bandera

# Bandera
picoCTF{thenumbersmason}

## Notas adicionales
| comando | descripción |
| ------ | ------ |
| xx | xx |

## Referencias
- []()