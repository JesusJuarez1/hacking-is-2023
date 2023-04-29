# HideToSee

# Objetivo
How about some hide and seek heh?Look at this image [here](https://artifacts.picoctf.net/c/237/atbash.jpg).

# Pistas
- Download the image and try to extract it

# Solución
- Descargamos la imagen
- Nos damos cuenta que dentro de la imagen hay algo mas y nos piden "extraerla"
- Nos damos cuenta que puede ser esteganografía
- Usamos el programa steghide "steghide extract -sf atbash.jpg"
- Con esto obtenemos un archivo txt que al hacer un cat nos da la bandera con un tipo de cifrado "krxlXGU{zgyzhs_xizxp_05y2z65z}" 
- Vamo a la pagina [cyberchef](https://gchq.github.io/CyberChef/) y le aplicamos el filtro de atbash que nos indica el nombre de la imagen
- Y con esto obtenemos la bandera

# Bandera
picoCTF{atbash_crack_05b2a65a}

## Notas adicionales
| comando | descripción |
| ------ | ------ |
| xx | xx |

## Referencias
- []()