# Enhance!

## Descripción
Download this image file and find the flag.
-   [Download image file](https://artifacts.picoctf.net/c/100/drawing.flag.svg)

## Solución
- Descargamos la imagen
- Al abrir la imagen no nos dice nada
- Le hacemos un strings y podemos ver que hay un patron el cual nos puede dar la bandera, este patron esta entre \<tspan>
```bash
┌──(kali㉿kali)-[~/picoctf/forensic/enhance]
└─$ strings drawing.flag.svg | grep "tspan"
       id="text3723"><tspan
         id="tspan3748">p </tspan><tspan
         id="tspan3754">i </tspan><tspan
         id="tspan3756">c </tspan><tspan
         id="tspan3758">o </tspan><tspan
         id="tspan3760">C </tspan><tspan
         id="tspan3762">T </tspan><tspan
         id="tspan3764">F { 3 n h 4 n </tspan><tspan
         id="tspan3752">c 3 d _ a a b 7 2 9 d d }</tspan></text>
```
- Al acomodar la bandera nos quedaria:
- picoCTF{3nh4nc3d_aab729dd}

## Bandera
picoCTF{3nh4nc3d_aab729dd}

## Notas adicionales
| comando | descripción |
| ------ | ------ |
| xx | xx |

## Referencias
- []()