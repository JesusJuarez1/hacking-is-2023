# Webnet1

# Objetivo
We found this [packet capture](https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/capture.pcap) and [key](https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/picopico.key). Recover the flag.

# Pistas
- Try using a tool like Wireshark.
- How can you decrypt the TLS stream?

# Solución
- Descargamos los dos archivos
- Abrimos la captura de paquetes con wireshark
- Los paquetes como en el reto anterior, estan encirptados
- Por lo que agregamos la llave que que descargamos
- Con esto desencriptamos algunos paquetes
- Nos damos cuenta que se esta descargando una imagen
- La extraemos con la opción de "export objects" de wireshark
- La guardamos y vamos a examinar la imagen
- Al abrir la imagen nos damos cuenta que ahí no hay nada
- Le aplicamos un strings y ahí es donde se encuentra la bandera
```
┌──(kali㉿kali)-[~/picoctf/forensic/WebNet1]
└─$ strings vulture.jpg | grep "picoCTF"
picoCTF{honey.roasted.peanuts}
```

# Bandera
picoCTF{honey.roasted.peanuts}

## Notas adicionales
| comando | descripción |
| ------ | ------ |
| xx | xx |

## Referencias
- []()