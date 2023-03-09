# dont-use-client-side

# Objetivo
Can you break into this super secure portal? `https://jupiter.challenges.picoctf.org/problem/17682/` ([link](https://jupiter.challenges.picoctf.org/problem/17682/)) or http://jupiter.challenges.picoctf.org:17682

# Pistas
- Never trust the client

# Solución
Inspeccionamos la pagina donde se llama la función para verificar la contraseña. Formamos la contraseña de como esta formada en los ifs que se encuentran en la función. Al final probamos la bandera en la pagina, si nos dice que la contraseña esta verificada, esa seria la bandera ya formada.

# Bandera
picoCTF{no_clients_plz_b706c5}

## Notas adicionales
| comando | descripción |
| ------ | ------ |
| xx | xx |

## Referencias
- []()