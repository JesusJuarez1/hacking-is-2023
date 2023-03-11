# Codebook

## Descripción
Run the Python script `code.py` in the same directory as `codebook.txt`.
-   [Download code.py](https://artifacts.picoctf.net/c/100/code.py)
-   [Download codebook.txt](https://artifacts.picoctf.net/c/100/codebook.txt)

## Pistas
- On the webshell, use `ls` to see if both files are in the directory you are in
- The `str_xor` function does not need to be reverse engineered for this challenge.

## Solución
```bash
jesjua-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/100/code.py
--2023-03-11 02:23:20--  https://artifacts.picoctf.net/c/100/code.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 108.156.172.74, 108.156.172.120, 108.156.172.42, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|108.156.172.74|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1278 (1.2K) [application/octet-stream]
Saving to: 'code.py'

code.py                                         100%[======================================================================================================>]   1.25K  --.-KB/s    in 0s      

2023-03-11 02:23:21 (430 MB/s) - 'code.py' saved [1278/1278]

jesjua-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/100/codebook.txt
--2023-03-11 02:23:33--  https://artifacts.picoctf.net/c/100/codebook.txt
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 108.156.172.74, 108.156.172.120, 108.156.172.42, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|108.156.172.74|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 27 [application/octet-stream]
Saving to: 'codebook.txt'

codebook.txt                                    100%[======================================================================================================>]      27  --.-KB/s    in 0s      

2023-03-11 02:23:33 (9.16 MB/s) - 'codebook.txt' saved [27/27]

jesjua-picoctf@webshell:~$ ls
code.py  codebook.txt
jesjua-picoctf@webshell:~$ python3 code.py 
picoCTF{c0d3b00k_455157_d9aa2df2}
jesjua-picoctf@webshell:~$
```

## Bandera
picoCTF{c0d3b00k_455157_d9aa2df2}

## Notas adicionales
| comando | descripción |
| ------ | ------ |
| xx | xx |

## Referencias
- []()