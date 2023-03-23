# So meta

# Objetivo
Find the flag in this [picture](https://jupiter.challenges.picoctf.org/static/916b07b4c87062c165ace1d3d31ef655/pico_img.png).

# Pistas
- What does meta mean in the context of files?
- Ever heard of metadata?

# Solución
```
┌──(kali㉿kali)-[~/picoctf/forensic/someta]
└─$ wget https://jupiter.challenges.picoctf.org/static/916b07b4c87062c165ace1d3d31ef655/pico_img.png
--2023-03-23 14:24:22--  https://jupiter.challenges.picoctf.org/static/916b07b4c87062c165ace1d3d31ef655/pico_img.png
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 108795 (106K) [application/octet-stream]
Saving to: ‘pico_img.png’

pico_img.png        100%[================>] 106.25K   419KB/s    in 0.3s    

2023-03-23 14:24:23 (419 KB/s) - ‘pico_img.png’ saved [108795/108795]

                                                               
┌──(kali㉿kali)-[~/picoctf/forensic/someta]
└─$ strings pico_img.png | grep "picoCTF" 
picoCTF{s0_m3ta_d8944929}K
                                                                             
┌──(kali㉿kali)-[~/picoctf/forensic/someta]
└─$ 

```

# Bandera
picoCTF{s0_m3ta_d8944929}

## Notas adicionales
| comando | descripción |
| ------ | ------ |
| xx | xx |

## Referencias
- []()