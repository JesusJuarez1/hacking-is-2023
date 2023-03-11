# Obedient Cat

## Descripción
This file has a flag in plain sight (aka "in-the-clear"). [Download flag](https://mercury.picoctf.net/static/a5683698ac318b47bd060cb786859f23/flag).

## Pistas
- Any hints about entering a command into the Terminal (such as the next one), will start with a '$'... everything after the dollar sign will be typed (or copy and pasted) into your Terminal.
- To get the file accessible in your shell, enter the following in the Terminal prompt: `$ wget https://mercury.picoctf.net/static/a5683698ac318b47bd060cb786859f23/flag`
- $ man cat

## Solución
```bash
jesjua-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/a5683698ac318b47bd060cb786859f23/flag
--2023-03-11 01:16:58--  https://mercury.picoctf.net/static/a5683698ac318b47bd060cb786859f23/flag
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 34 [application/octet-stream]
Saving to: 'flag'

flag                                            100%[======================================================================================================>]      34  --.-KB/s    in 0s      

2023-03-11 01:16:58 (16.6 MB/s) - 'flag' saved [34/34]

jesjua-picoctf@webshell:~$ ls
README.txt  file  flag  strings
jesjua-picoctf@webshell:~$ cat flag
picoCTF{s4n1ty_v3r1f13d_4a2b35fd}
jesjua-picoctf@webshell:~$
```

## Bandera
picoCTF{s4n1ty_v3r1f13d_4a2b35fd}

## Notas adicionales
| comando | descripción |
| ------ | ------ |
| xx | xx |

## Referencias
- []()