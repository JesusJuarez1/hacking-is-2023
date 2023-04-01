# WebNet0

# Objetivo
We found this [packet capture](https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/capture.pcap) and [key](https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/picopico.key). Recover the flag.

# Pistas
- Try using a tool like Wireshark.
- How can you decrypt the TLS stream?

# Solución
- Descargamos los dos archivos 
- Cargamos el archivo "capture.pcap" en wireshark
- Como todos los paqutes estan encriptados no podemos ver su contenido
- Cargamos el archivo "picopico.key" en la lista de protocolos/TLS/ agregar una llave
- Con esto se desencriptan los paquetes y podemo hacer una busqueda para encontrar la llave
- Luego hacemos una busqueda en los detalles de los paquetes buscando la cadena "picoCTF" y con esto encontramos la bandera

# Bandera
picoCTF{nongshim.shrimp.crackers}

## Notas adicionales
| comando | descripción |
| ------ | ------ |
| xx | xx |

## Referencias
- []()