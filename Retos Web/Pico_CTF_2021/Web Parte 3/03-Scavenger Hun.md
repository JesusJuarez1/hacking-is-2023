# Scavenger Hun

# Objetivo
There is some interesting information hidden around this site [http://mercury.picoctf.net:55079/](http://mercury.picoctf.net:55079/). Can you find it?

# Pistas
- You should have enough hints to find the files, don't run a brute forcer.

# Solución
- Ingresamos a la pagina
- La pagina nos dice lo que utilizo para realizar el sitio, por lo que nos damos una idea donde puede estar la bandera
- Inspeccionamos el codigo y nos damos cuenta que la primera parte de la bandera esta en un comentario del html "picoCTF{t"
- Luego vamos a inspeccionar el css y encontramos la segunda parte de la bandera "h4ts_4_l0"
- Por ultimo inspeccionamos el js de la pagina y encontramos una pista de donde podria estar la tercera parte de la bandera
- Colocamos "robots.txt" al final de la url de la pagina
- Y ahí encontramos la tercera parte de la bandera "t_0f_pl4c" y una pista a la cuarta parte de la vandera
- Ingresamos al archivo .htaccess y ahí encontramos la siguiente parte y otra pista "3s_2_lO0k"
- Y por ultimo ingresamos al alchivo .DS_Store en donde se encuentra la ultima parte de la bandera "_74cceb07}"

# Bandera
picoCTF{th4ts_4_l0t_0f_pl4c3s_2_lO0k_74cceb07}

## Notas adicionales
| comando | descripción |
| ------ | ------ |
| xx | xx |

## Referencias
- []()