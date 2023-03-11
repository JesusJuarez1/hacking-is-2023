# Static ain't always noise

## Descripción
Can you look at the data in this binary: [static](https://mercury.picoctf.net/static/e9dd71b5d11023873b8abe99cdb45551/static)? This [BASH script](https://mercury.picoctf.net/static/e9dd71b5d11023873b8abe99cdb45551/ltdis.sh) might help!

## Pistas
- 

## Solución
```bash
jesjua-picoctf@webshell:~$ ls
ltdis.sh  static  warm            
jesjua-picoctf@webshell:~$ chmod +x ltdis.sh 
jesjua-picoctf@webshell:~$ chmod +x static
jesjua-picoctf@webshell:~$ ls
ltdis.sh  static  warm
jesjua-picoctf@webshell:~$ ./ltdis.sh 
Attempting disassembly of  ...
objdump: 'a.out': No such file
objdump: section '.text' mentioned in a -j option, but not found in any input file
Disassembly failed!
Usage: ltdis.sh <program-file>
Bye!
jesjua-picoctf@webshell:~$ ^C
jesjua-picoctf@webshell:~$ ./ltdis.sh static 
Attempting disassembly of static ...
Disassembly successful! Available at: static.ltdis.x86_64.txt
Ripping strings from binary with file offsets...
Any strings found in static have been written to static.ltdis.strings.txt with file offset
jesjua-picoctf@webshell:~$ ls
ltdis.sh  static  static.ltdis.strings.txt  static.ltdis.x86_64.txt  warm
jesjua-picoctf@webshell:~$ cat static.ltdis.strings.txt | grep "pico"
   1020 picoCTF{d15a5m_t34s3r_ae0b3ef2}
jesjua-picoctf@webshell:~$
```

## Bandera
picoCTF{d15a5m_t34s3r_ae0b3ef2}

## Notas adicionales
| comando | descripción |
| ------ | ------ |
| xx | xx |

## Referencias
- []()