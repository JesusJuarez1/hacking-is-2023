# Irish-Name-Repo 2

# Objetivo
There is a website running at `https://jupiter.challenges.picoctf.org/problem/52849/` ([link](https://jupiter.challenges.picoctf.org/problem/52849/)). Someone has bypassed the login before, and now it's being strengthened. Try to see if you can still login! or http://jupiter.challenges.picoctf.org:52849

# Pistas
- The password is being filtered.

# Solución
- Ingresamos al link.
- Tratamos de hacer lo mismo que en el reto anterior, sin embargo nos detecta que inyectamos codigo sql.
- Aunque no nos funcione el metodo anterior seguimos viendo la sentencia que se utiliza.
- Identificamos que si colocamos **admin';** esto hara que la sentencia se termine en cuanto consulte el usuario admin y con esto nos dejara entrar.

# Bandera
picoCTF{m0R3_SQL_plz_fa983901}

## Notas adicionales
| comando | descripción |
| ------ | ------ |
| xx | xx |

## Referencias
- []()