# two-sum

# Objetivo
Can you solve this?What two positive numbers can make this possible: `n1 > n1 + n2 OR n2 > n1 + n2`Enter them here `nc saturn.picoctf.net 65398`. [Source](https://artifacts.picoctf.net/c/456/flag.c)

# Pistas
- Integer overflow
- Not necessarily a math problem

# Solución
- Primero descargamos el codigo y lo inspeccionamos
- Nos damos cuenta que la condicion es imposible que sea valida
- Con las pistas nos damos una idea de lo que puede hacerse
- El numero maximo permitido por un entero en c es de 32 bits (2,147,483,647)
- Por lo que un numero mayor a este dara como resultado -1 de error
- Pero no ingresamos un numero como este de parametro si no que hacemos que dos numeros sumados den un numero mas grande que el antes mencionado y provocar que el resultado genere -1 y con esto la condicion se cumple y nos entrega la bandera
```
jesjua-picoctf@webshell:~$ nc saturn.picoctf.net 65398
n1 > n1 + n2 OR n2 > n1 + n2 
What two positive numbers can make this possible: 
1234567890
1234567890
You entered 1234567890 and 1234567890
You have an integer overflow
YOUR FLAG IS: picoCTF{Tw0_Sum_Integer_Bu773R_0v3rfl0w_ccd078bd}
```

# Bandera
picoCTF{Tw0_Sum_Integer_Bu773R_0v3rfl0w_ccd078bd}

## Notas adicionales
| comando | descripción |
| ------ | ------ |
| xx | xx |

## Referencias
- []()