# Wireshark doo dooo do doo..

## Descripción
Can you find the flag? [shark1.pcapng](https://mercury.picoctf.net/static/4c996ecfb7fbada15a9799511f24dc99/shark1.pcapng).

## Solución
- Descargamos el archivo
- Lo cargamos en la herramienta de whireshark
- Ahí vemos que hay una conversacion entre dos computadoras utilizando el protocolo HTTP
- Damos click derecho sobre el primero, luego "follow/TCP stream"
- Ahi vamos recorriendo entre la conversación buscando algo entre los paquetes que nos pueda servir
- En el paquete numero 5 encontramos un texto que tiene el la apariencia de la bandera pero parece estar rotada
- En la pagina [cyberchef](https://gchq.github.io/CyberChef/#recipe=ROT13(true,true,false,13)&input=Y3ZwYlBHU3tjMzN4bm8wMF8xX2YzM19oX3FybnFvcnJzfQ) y le aplicamos el filtro de rot13
- Con esto obtenemos la bandera

## Bandera
picoCTF{p33kab00_1_s33_u_deadbeef}

## Notas adicionales
| comando | descripción |
| ------ | ------ |
| xx | xx |

## Referencias
- []()