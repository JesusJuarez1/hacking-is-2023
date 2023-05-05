# SQL Direct

## Descripción
Connect to this PostgreSQL server and find the flag!
Additional details will be available after launching your challenge instance.
Connect to this PostgreSQL server and find the flag! `psql -h saturn.picoctf.net -p 57587 -U postgres pico` Password is `postgres`

## Pistas
- 

## Solución
- Nos conectamos a la base de datos que nos dan
- "consultamos" que tablas tiene la base de datos
```bash
pico=# \dt
         List of relations
 Schema | Name  | Type  |  Owner   
--------+-------+-------+----------
 public | flags | table | postgres
(1 row)
```
- Luego de esto hacemos una consulta a la tabla flags
```bash
pico=# SELECT * FROM FLAGS;
 id | firstname | lastname  |                address                 
----+-----------+-----------+----------------------------------------
  1 | Luke      | Skywalker | picoCTF{L3arN_S0m3_5qL_t0d4Y_73b0678f}
  2 | Leia      | Organa    | Alderaan
  3 | Han       | Solo      | Corellia
(3 rows)
```
- Con esto obtenemos la bandera

## Bandera
picoCTF{L3arN_S0m3_5qL_t0d4Y_73b0678f}

## Notas adicionales
| comando | descripción |
| ------ | ------ |
| \\dt | Nos dice que tablas existen en una base de datos postgres |

## Referencias
- []()