# Bases

## Descripción
What does this `bDNhcm5fdGgzX3IwcDM1` mean? I think it has something to do with bases.

## Pistas
- Submit your answer in our flag format. For example, if your answer was 'hello', you would submit 'picoCTF{hello}' as the flag.

## Solución
```bash
jesjua-picoctf@webshell:~$ echo "bDNhcm5fdGgzX3IwcDM1" | base64 --      
--decode          --help            --ignore-garbage  --version         --wrap=           
jesjua-picoctf@webshell:~$ echo "bDNhcm5fdGgzX3IwcDM1" | base64 --decode 
l3arn_th3_r0p35
jesjua-picoctf@webshell:~$
```

## Bandera
picoCTF{l3arn_th3_r0p35}

## Notas adicionales
| comando | descripción |
| ------ | ------ |
| xx | xx |

## Referencias
- [base64](https://ubunlog.com/base64-codificacion-decodificacion-terminal/?utm_source=feedburner&utm_medium=%24%7Bfeed%2C+email%7D&utm_campaign=Feed%3A+%24%7BUbunlog%7D+%28%24%7BUbunlog%7D%29)