# fixme2.py

## Descripción
Fix the syntax error in the Python script to print the flag.[Download Python script](https://artifacts.picoctf.net/c/66/fixme2.py)

## Pistas
- Are equality and assignment the same symbol?
- To view the file in the webshell, do: `$ nano fixme2.py`
- To exit `nano`, press Ctrl and x and follow the on-screen prompts.
- The `str_xor` function does not need to be reverse engineered for this challenge.

## Solución
```bash
jesjua-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/66/fixme2.py
--2023-03-11 03:04:14--  https://artifacts.picoctf.net/c/66/fixme2.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 108.156.172.120, 108.156.172.42, 108.156.172.6, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|108.156.172.120|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1029 (1.0K) [application/octet-stream]
Saving to: 'fixme2.py'

fixme2.py                                       100%[======================================================================================================>]   1.00K  --.-KB/s    in 0.002s  

2023-03-11 03:04:14 (547 KB/s) - 'fixme2.py' saved [1029/1029]

jesjua-picoctf@webshell:~$ ls
README.txt  fixme2.py
jesjua-picoctf@webshell:~$ python3 fixme2.py 
  File "/home/jesjua-picoctf/fixme2.py", line 22
    if flag = "":
       ^^^^^^^^^
SyntaxError: invalid syntax. Maybe you meant '==' or ':=' instead of '='?
jesjua-picoctf@webshell:~$ nano fixme2.py 
jesjua-picoctf@webshell:~$ python3 fixme2.py 
That is correct! Here's your flag: picoCTF{3qu4l1ty_n0t_4551gnm3nt_4863e11b}
jesjua-picoctf@webshell:~$ 
```

## Bandera
picoCTF{3qu4l1ty_n0t_4551gnm3nt_4863e11b}

## Notas adicionales
| comando | descripción |
| ------ | ------ |
| xx | xx |

## Referencias
- []()