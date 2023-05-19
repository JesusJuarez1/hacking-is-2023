# Mr-Worldwide

# Objetivo
A musician left us a [message](https://jupiter.challenges.picoctf.org/static/d5570d48262dbba2a31f2a940409ad9d/message.txt). What's it mean?

# Pistas

# Solución
- Descargamos el archivo
- Le hacemos un cat y nos muestra la bandera en formato de coordenadas
- Buscamos las cordenadas
```
picoCTF{(35.028309, 135.753082)(46.469391, 30.740883)(39.758949, -84.191605)(41.015137, 28.979530)(24.466667, 54.366669)(3.140853, 101.693207)_(9.005401, 38.763611)(-3.989038, -79.203560)(52.377956, 4.897070)(41.085651, -73.858467)(57.790001, -152.407227)(31.205753, 29.924526)}
```
| coordenadas | Ciudad |
| --- | --- |
| 35.028309, 135.753082 | Kioto |
| 46.469391, 30.740883 | Odesa |
| 39.758949, -84.191605 | Dayton |
| 41.015137, 28.979530 | Istanbul |
| 24.466667, 54.366669 | Abu Dhabi |
| 3.140853, 101.693207 | Kuala |
| 9.005401, 38.763611 | Addis |
| -3.989038, -79.203560 | Loja |
| 52.377956, 4.897070 | Amsterdam |
| 41.085651, -73.858467 | Sleepy |
| 57.790001, -152.407227 | Kodiak |
| 31.205753, 29.924526 | Alexandria |
- Juantando la primera letra de cada ciudad se obtiene la bandera

# Bandera
picoCTF{KODIAK_ALASKA}

## Notas adicionales
| comando | descripción |
| ------ | ------ |
| xx | xx |

## Referencias
- []()