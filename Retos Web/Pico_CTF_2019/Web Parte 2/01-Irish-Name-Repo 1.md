# Irish-Name-Repo 1

# Objetivo
There is a website running at `https://jupiter.challenges.picoctf.org/problem/39720/` ([link](https://jupiter.challenges.picoctf.org/problem/39720/)) or http://jupiter.challenges.picoctf.org:39720. Do you think you can log us in? Try to see if you can login!

# Pistas
- There doesn't seem to be many ways to interact with this. I wonder if the users are kept in a database?
- Try to think about how the website verifies your login.

# Solución
- Ingresamos a la liga
- Hacemos el elemento oculto como visible quitando el hidden
- En ese campo agregamos un 1 en vez del 0 que tenia. Con esto nos da la sentencia sql con la que hace la consulta.
- username: jesus
	password: jesus
	SQL query: SELECT * FROM users WHERE name='jesus' AND password='jesus' 
- Como sabemos la sintaxis de la sentencia hacemos que esta sentencia sea verdadera
- colocando el **' or 1=1;** en el usuario o contraseña


# Bandera
picoCTF{s0m3_SQL_c218b685}

## Notas adicionales
| comando | descripción |
| ------ | ------ |
| xx | xx |

## Referencias
- []()