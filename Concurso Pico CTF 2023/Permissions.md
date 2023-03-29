# Permissions

# Objetivo
Can you read files in the root file?

# Pistas
- What permissions do you have?

# Solución
```
picoplayer@challenge:~~$ cd root 
-bash: cd: root: No such file or directory 
picoplayer@challenge:~$ cd / 
picoplayer@challenge:/$ ls 
bin challenge etc lib lib64 media opt root sbin sys usr boot dev home lib32 libx32 mnt proc run srv tmp var 
picoplayer@challenge:/$ cat challenge 
cat: challenge: Is a directory 
picoplayer@challenge:/$ cd challenge/ 
picoplayer@challenge:/challenge$ ls 
metadata.json 
picoplayer@challenge:/challenge$ cat metadata.json 
{"flag": "picoCTF{uS1ng_v1m_3dit0r_89e9cf1a}", 
"username": "picoplayer", 
"password": "Sd9KYTm5kr"}
```

# Bandera
picoCTF{uS1ng_v1m_3dit0r_89e9cf1a}

## Notas adicionales
| comando | descripción |
| ------ | ------ |
| xx | xx |

## Referencias
- []()