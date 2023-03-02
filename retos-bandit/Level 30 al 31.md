# Bandit Level 30 al Level 31

## Objetivo
There is a git repository at `ssh://bandit30-git@localhost/home/bandit30-git/repo`. The password for the user `bandit30-git` is the same as for the user `bandit30`.
Clone the repository and find the password for the next level.

## Datos de acceso
bandit30
xbhV3HpNGlTIdnjUrdAlPzc2L6y9EOnS

## Solución
```bash
bandit30@bandit:~$ mktemp -d
/tmp/tmp.NaOk6XRdaZ
bandit30@bandit:~$ cd /tmp/tmp.NaOk6XRdaZ
bandit30@bandit:/tmp/tmp.NaOk6XRdaZ$ git clone ssh://bandit30-git@localhost:2220/home/bandit30-git/repo
Cloning into 'repo'...
The authenticity of host '[localhost]:2220 ([127.0.0.1]:2220)' can't be established.
ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Could not create directory '/home/bandit30/.ssh' (Permission denied).
Failed to add the host to the list of known hosts (/home/bandit30/.ssh/known_hosts).
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit30-git@localhost's password:
Permission denied, please try again.
bandit30-git@localhost's password:
remote: Enumerating objects: 4, done.
remote: Counting objects: 100% (4/4), done.
remote: Total 4 (delta 0), reused 0 (delta 0), pack-reused 0
Receiving objects: 100% (4/4), 299 bytes | 299.00 KiB/s, done.
bandit30@bandit:/tmp/tmp.NaOk6XRdaZ$ ls
repo
bandit30@bandit:/tmp/tmp.NaOk6XRdaZ$ cd repo/
bandit30@bandit:/tmp/tmp.NaOk6XRdaZ/repo$ ls
README.md
bandit30@bandit:/tmp/tmp.NaOk6XRdaZ/repo$ cat README.md
just an epmty file... muahaha
bandit30@bandit:/tmp/tmp.NaOk6XRdaZ/repo$ git log
commit cf552c166d78421e64ddf52f850e680075d216e1 (HEAD -> master, origin/master, origin/HEAD)
Author: Ben Dover <noone@overthewire.org>
Date:   Tue Feb 21 22:03:13 2023 +0000

    initial commit of README.md
bandit30@bandit:/tmp/tmp.NaOk6XRdaZ/repo$ git log -p -1
commit cf552c166d78421e64ddf52f850e680075d216e1 (HEAD -> master, origin/master, origin/HEAD)
Author: Ben Dover <noone@overthewire.org>
Date:   Tue Feb 21 22:03:13 2023 +0000

    initial commit of README.md

diff --git a/README.md b/README.md
new file mode 100644
index 0000000..029ba42
--- /dev/null
+++ b/README.md
@@ -0,0 +1 @@
+just an epmty file... muahaha
bandit30@bandit:/tmp/tmp.NaOk6XRdaZ/repo$ git tag
secret
bandit30@bandit:/tmp/tmp.NaOk6XRdaZ/repo$ git show secret
OoffzGDlzhAlerFJ2cAiz1D41JW1Mhmt
bandit30@bandit:/tmp/tmp.NaOk6XRdaZ/repo$
```

## Notas adicionales
| comando | descripción |
| ------ | ------ |
| git tag | Muestra todas las etiquetas del repositorio |
| git show | Muestra el contenido de la etiqueta junto al commit etiquetado |

## Referencias
- []()