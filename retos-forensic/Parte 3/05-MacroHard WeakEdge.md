# MacroHard WeakEdge

# Objetivo
I've hidden a flag in this file. Can you find it? [Forensics is fun.pptm](https://mercury.picoctf.net/static/c00c449c3b08daaccacca6f9d5c55d49/Forensics is fun.pptm)

# Solución
- Descargamos el archivo
- Nos dice que es un archivo de power point con una macro activada
- Desempaquetamos el archivo
- Abrimos la estructura del carpetas en visual code para explorar mejor los archivos
- Nos encontramos con un archivo que contiene una cadena en base 64
- Copiamos la cadena para convertirla en texto
```
┌──(kali㉿kali)-[~/picoctf/forensic/MacroHardWeakEdge]
└─$ echo "Z m x h Z z o g c G l j b 0 N U R n t E M W R f d V 9 r b j B 3 X 3 B w d H N f c l 9 6 M X A 1 f Q" | tr -d " " | base64 -d
flag: picoCTF{D1d_u_kn0w_ppts_r_z1p5}base64: invalid input
```
- Haciendo esto obtenemos la bandera

# Bandera
picoCTF{D1d_u_kn0w_ppts_r_z1p5}

## Notas adicionales
| comando | descripción |
| ------ | ------ |
| xx | xx |

## Referencias
- []()