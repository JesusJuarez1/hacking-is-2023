# Power Cookie

## Descripción
Can you get the flag? Go to this [website](http://saturn.picoctf.net:65442/) and see what you can discover.

## Pistas
- Do you know how to modify cookies?

## Solución
- Ingresamos a la pagina
- Vemos que el reto esta en las cookies
- Vemos que la primera vez que damos al boton "continue as gest" nos guarda una cookie la cual es una funcion preguntando si es administrador y nos la guarda en 0
- Volvemos a cargar la pagina y ya no nos guarda ese valor asi que agregamos una cookie manualmente con la funcion "isAdmin" con el valor en 1
- La guardamos y recargamos la pagina y esta nos da la bandera

## Bandera
picoCTF{gr4d3_A_c00k13_5d2505be}

## Notas adicionales
| comando | descripción |
| ------ | ------ |
| xx | xx |

## Referencias
- []()