
# Bandit Level 22 al Level 23

## Objetivo
A program is running automatically at regular intervals from **cron**, the time-based job scheduler. Look in **/etc/cron.d/** for the configuration and see what command is being executed.

## Datos de acceso
bandit22
WdDozAdTM2z9DiFEQ2mGlwngMfj4EZff

## Solución
```bash
bandit22@bandit:~$ cat /etc/cron.d/cronjob_bandit23
@reboot bandit23 /usr/bin/cronjob_bandit23.sh  &> /dev/null
* * * * * bandit23 /usr/bin/cronjob_bandit23.sh  &> /dev/null
bandit22@bandit:~$ cat /usr/bin/cronjob_bandit23.sh
#!/bin/bash

myname=$(whoami)
mytarget=$(echo I am user $myname | md5sum | cut -d ' ' -f 1)

echo "Copying passwordfile /etc/bandit_pass/$myname to /tmp/$mytarget"

cat /etc/bandit_pass/$myname > /tmp/$mytarget
bandit22@bandit:~$ myname=bandit23
bandit22@bandit:~$ echo $bandit23

bandit22@bandit:~$ echo I am user %myname
I am user %myname
bandit22@bandit:~$ echo I am user $myname
I am user bandit23
bandit22@bandit:~$ echo I am user $myname | md5sum
8ca319486bfbbc3663ea0fbe81326349  -
bandit22@bandit:~$ echo I am user $myname | md5sum | cut -d ' ' -f 1
8ca319486bfbbc3663ea0fbe81326349
bandit22@bandit:~$ echo $(echo I am user $myname | md5sum | cut -d ' ' -f 1)
8ca319486bfbbc3663ea0fbe81326349
bandit22@bandit:~$ cat /tmp/8ca319486bfbbc3663ea0fbe81326349
QYw0Y2aiA672PsMmh9puTQuhoz8SyR2G
```

## Notas adicionales
| comando | descripción |
| ------ | ------ |
| md5sum | Obtiene el hash de un parametro |

## Referencias
- []()