# Pixelated

# Objetivo
I have these 2 images, can you make a flag out of them? [scrambled1.png](https://mercury.picoctf.net/static/75e646e4ad19967ca1811f895fb40465/scrambled1.png) [scrambled2.png](https://mercury.picoctf.net/static/75e646e4ad19967ca1811f895fb40465/scrambled2.png)

# Pistas
- [https://en.wikipedia.org/wiki/Visual_cryptography](https://en.wikipedia.org/wiki/Visual_cryptography)
- Think of different ways you can "stack" images

# Solución
- Descargamos las imagenes
- Descargamos la herramienta con "wget http://www.caesum.com/handbook/Stegsolve.jar -O stegsolve.jar"
- Luego le damos permisos de ejecución con "chmod +x stegsolve.jar"
- Luego la corremos con
```
┌──(kali㉿kali)-[~/picoctf/crypto/pixelated]
└─$ java -jar /opt/stegsolve.jar 
Picked up _JAVA_OPTIONS: -Dawt.useSystemAAFontSettings=on -Dswing.aatext=true
```
- Esto nos abrira una ventana en la que abriremos la primera imagen dandole file/open
- Luego le damos en Analyse/Image Conbiner y abrimos la segunda imagen
- Esto nos abrira una nueva ventana en la que vamos dando click en > para ir cambiando de modo
- Cambiamos al modo ADD
- Y con esto podremos ver la bandera en la imagen

# Bandera
picoCTF{d562333d}

## Notas adicionales
| comando | descripción |
| ------ | ------ |
| xx | xx |

## Referencias
- []()