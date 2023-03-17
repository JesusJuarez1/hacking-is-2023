# GET aHEAD

# Objetivo
Find the flag being held on this server to get ahead of the competition [http://mercury.picoctf.net:28916/](http://mercury.picoctf.net:28916/)

# Pistas
- Maybe you have more than 2 choices
- Check out tools like Burpsuite to modify your requests and look at the responses

# Solución
- Ingresamos a la pagina y vemos que solo nos deja cambiar de color el fondo de la pagina
- Inspeccionamos la pagina y vemos que un boton hace peticion por GET y otro por POST
- Vemos la pestaña de red y vamos a reenviar la petición cambiando el metodo GET por HEAD
- Y con esto nos da la bandera en la parte de encabezados de respuesta

# Bandera
picoCTF{r3j3ct_th3_du4l1ty_70bc61c4}

## Notas adicionales
| comando | descripción |
| ------ | ------ |
| xx | xx |

## Referencias
- []()