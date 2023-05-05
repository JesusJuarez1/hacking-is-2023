# Packets Primer

## Descripción
Download the packet capture file and use packet analysis software to find the flag.
-   [Download packet capture](https://artifacts.picoctf.net/c/195/network-dump.flag.pcap)

## Pistas
- Wireshark, if you can install and use it, is probably the most beginner friendly packet analysis software product.

## Solución
- Descargamos el archivo
- Lo cargamos en la herramienta de whireshark
- Al primer paquete le damos en "follow/TCP stream"
- En el primer paquete esta la bandera pero con espacios entre cada caracter
- Se los quitamos manualmente y listo obtenemos la bandera

## Bandera
picoCTF{p4ck37_5h4rk_b9d53765}

## Notas adicionales
| comando | descripción |
| ------ | ------ |
| xx | xx |

## Referencias
- []()