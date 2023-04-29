# Mind your Ps and Qs

# Objetivo
In RSA, a small `e` value can be problematic, but what about `N`? Can you decrypt this? [values](https://mercury.picoctf.net/static/bf5e2c8811afb4669f4a6850e097e8aa/values)

# Pistas
- Bits are expensive, I used only a little bit over 100 to save money

# Solución
- Descargamos el archivo que nos dan
- Vemos su contenido con un cat
```
Decrypt my super sick RSA:
c: 421345306292040663864066688931456845278496274597031632020995583473619804626233684
n: 631371953793368771804570727896887140714495090919073481680274581226742748040342637
e: 65537 
```
- Nos damos cuenta que nos da un texto encryptado
- Vamo a la pagina [factordb](http://factordb.com/index.php?query=631371953793368771804570727896887140714495090919073481680274581226742748040342637)
- Con esto obtenemos p y q y ya podremos desencriptar el mensaje
```
>> from Crypto.Util.number import long_to_bytes
>>> from Crypto.Util.number import inverse>>> c = 421345306292040663864066688931456845278496274597031632020995583473619804626233684
>>> e = 65537
>>> p = 1461849912200000206276283741896701133693
>>> q = 431899300006243611356963607089521499045809
>>> n = p*q
>>> n
631371953793368771804570727896887140714495090919073481680274581226742748040342637
>>> tn = (p-1)*(q-1)
>>> d = inverse(e,tn)
>>> m=pow(c,d,n)
>>> long_to_bytes(m)
b'picoCTF{sma11_N_n0_g0od_55304594}'
```

# Bandera
picoCTF{sma11_N_n0_g0od_55304594}

## Notas adicionales
| comando | descripción |
| ------ | ------ |
| xx | xx |

## Referencias
- []()