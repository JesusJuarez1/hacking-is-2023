# Cookies

# Objetivo
Who doesn't love cookies? Try to figure out the best one. [http://mercury.picoctf.net:64944/](http://mercury.picoctf.net:64944/)

# Pistas

# Solución
- Ingresamos a la pagina
- Con el burp activo en froxy proxy y la aplicación de burp de kali ingresamos enviamos una cookie
- Con esto obtenemos la petición
- Enviamos la petición al intruder dentro de la aplicación Brup
- Hacemos un ataque de tipo sniper
- En payloads le decimos que haga peticiones cambiando la cookie con un rango del 1 al 21
- Y le damos a atacar
- Con esto en las respuestas buscamos "picoCTF{" con esto navegamos en las respuestas hasta que haya una coincidencia

# Bandera
picoCTF{3v3ry1_l0v3s_c00k135_cc9110ba}

## Notas adicionales
| comando | descripción |
| ------ | ------ |
| xx | xx |

## Referencias
- []()