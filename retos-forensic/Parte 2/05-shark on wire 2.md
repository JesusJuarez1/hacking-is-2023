# shark on wire 2

# Objetivo
We found this [packet capture](https://jupiter.challenges.picoctf.org/static/b506393b6f9d53b94011df000c534759/capture.pcap). Recover the flag that was pilfered from the network.

# Pistas

# Solución
- Descargamos el archivo
- Lo abrimos en wireshark
- identificamos uno de los primero paquetes UDP el cual vamos a seguir el stream de ese paquete
- Identificamos que en el paquete 32 esta start y en el 60 end
- Filtramos todos los paquetes cuyo destino sea el puerto 22
- Nos damos cuenta que los puertos cambian a exepción de los paquetes start y end
- Los purtos que utiliza es la bandera en codigo ascii
- Creamos un exploy.py con el cual vamos a obtener la bandera mas facilmente
```
from scapy.all import *

packets = rdpcap('capture.pcap')
flag = ''
for p in packets:
        if UDP in p and p[UDP].dport == 22:
                if p[UDP].sport > 5000:   
                        flag += chr(p[UDP].sport-5000)
print(flag)
```
- Con esto ya solo ejecutamos el cosigo y obtenemos la bandera

# Bandera
picoCTF{p1LLf3r3d_data_v1a_st3g0}

## Notas adicionales
| comando | descripción |
| ------ | ------ |
| xx | xx |

## Referencias
- []()