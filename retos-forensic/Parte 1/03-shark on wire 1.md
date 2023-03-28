# ### shark on wire 1

# Objetivo
We found this [packet capture](https://jupiter.challenges.picoctf.org/static/483e50268fe7e015c49caf51a69063d0/capture.pcap). Recover the flag.

# Pistas
- Try using a tool like Wireshark
- What are streams?

# Solución
- Descargamos el archivo
- Lo abrimos con la aplicación wireshark de kali
- Le damos clic derecho al primer UDP, le damos a follow y luego a UDP Stream
- Esto nos mostrara lo que lleva cada UDP y nevegamos entre todas las UDP hasta encontrar la que contiene la bandera

# Bandera
picoCTF{StaT31355_636f6e6e}

## Notas adicionales
| comando | descripción |
| ------ | ------ |
| xx | xx |

## Referencias
- []()