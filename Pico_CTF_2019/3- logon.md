# logon

# Objetivo
The factory is hiding things from all of its users. Can you login as Joe and find what they've been looking at? `https://jupiter.challenges.picoctf.org/problem/44573/` ([link](https://jupiter.challenges.picoctf.org/problem/44573/)) or http://jupiter.challenges.picoctf.org:44573

# Pistas
- Hmm it doesn't seem to check anyone's password, except for Joe's?

# Solución
Intentamos logearnos con el usuario Joe pero como no tenemos la clave no podemos ingresar.
Con cualquier otro usuario y contraseña podemos ingresar pero no podemos ver la bandera.
Modificamos la cookie donde cambiamos el valor de admin de False a True, y con esto podemos ver la bandera

# Bandera
picoCTF{th3_c0nsp1r4cy_l1v3s_0c98aacc}

## Notas adicionales
| comando | descripción |
| ------ | ------ |
| xx | xx |

## Referencias
- []()