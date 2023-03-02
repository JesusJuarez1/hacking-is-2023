# Bandit Level 29 al Level 30

## Objetivo
There is a git repository at `ssh://bandit29-git@localhost/home/bandit29-git/repo`. The password for the user `bandit29-git` is the same as for the user `bandit29`.
Clone the repository and find the password for the next level.

## Datos de acceso
bandit29
tQKvmcwNYcFS6vmPHIUSI3ShmsrQZK8S

## Solución
```bash
bandit29@bandit:~$ mktemp -d
/tmp/tmp.v5dhVzl806
bandit29@bandit:~$ cd /tmp/tmp.v5dhVzl806
bandit29@bandit:/tmp/tmp.v5dhVzl806$ git clone ssh://bandit29-git@localhost:2220/home/bandit29-git/repo
Cloning into 'repo'...
The authenticity of host '[localhost]:2220 ([127.0.0.1]:2220)' can't be established.
ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Could not create directory '/home/bandit29/.ssh' (Permission denied).
Failed to add the host to the list of known hosts (/home/bandit29/.ssh/known_hosts).
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit29-git@localhost's password:
remote: Enumerating objects: 16, done.
remote: Counting objects: 100% (16/16), done.
remote: Compressing objects: 100% (11/11), done.
remote: Total 16 (delta 2), reused 0 (delta 0), pack-reused 0
Receiving objects: 100% (16/16), done.
Resolving deltas: 100% (2/2), done.
bandit29@bandit:/tmp/tmp.v5dhVzl806$ ls -la
total 124
drwx------   3 bandit29 bandit29   4096 Mar  1 23:27 .
drwxrwx-wt 838 root     root     114688 Mar  1 23:28 ..
drwxrwxr-x   3 bandit29 bandit29   4096 Mar  1 23:28 repo
bandit29@bandit:/tmp/tmp.v5dhVzl806$ cd repo/
bandit29@bandit:/tmp/tmp.v5dhVzl806/repo$ ls -la
total 16
drwxrwxr-x 3 bandit29 bandit29 4096 Mar  1 23:28 .
drwx------ 3 bandit29 bandit29 4096 Mar  1 23:27 ..
drwxrwxr-x 8 bandit29 bandit29 4096 Mar  1 23:28 .git
-rw-rw-r-- 1 bandit29 bandit29  131 Mar  1 23:28 README.md
bandit29@bandit:/tmp/tmp.v5dhVzl806/repo$ cat README.md
# Bandit Notes
Some notes for bandit30 of bandit.

## credentials

- username: bandit30
- password: <no passwords in production!>

bandit29@bandit:/tmp/tmp.v5dhVzl806/repo$ git log
commit 0afe3501277395fbfa017480925edee3df6e8bb5 (HEAD -> master, origin/master, origin/HEAD)
Author: Ben Dover <noone@overthewire.org>
Date:   Tue Feb 21 22:03:11 2023 +0000

    fix username

commit c2606dfc0aef7179bf1ccd6cffa9ed19151facb4
Author: Ben Dover <noone@overthewire.org>
Date:   Tue Feb 21 22:03:11 2023 +0000

    initial commit of README.md
bandit29@bandit:/tmp/tmp.v5dhVzl806/repo$ git log -p -1
commit 0afe3501277395fbfa017480925edee3df6e8bb5 (HEAD -> master, origin/master, origin/HEAD)
Author: Ben Dover <noone@overthewire.org>
Date:   Tue Feb 21 22:03:11 2023 +0000

    fix username

diff --git a/README.md b/README.md
index 2da2f39..1af21d3 100644
--- a/README.md
+++ b/README.md
@@ -3,6 +3,6 @@ Some notes for bandit30 of bandit.

 ## credentials

-- username: bandit29
+- username: bandit30
 - password: <no passwords in production!>

bandit29@bandit:/tmp/tmp.v5dhVzl806/repo$ cat README.md
# Bandit Notes
Some notes for bandit30 of bandit.

## credentials

- username: bandit30
- password: <no passwords in production!>
bandit29@bandit:/tmp/tmp.v5dhVzl806/repo$ git branch -r
  origin/HEAD -> origin/master
  origin/dev
  origin/master
  origin/sploits-dev
bandit29@bandit:/tmp/tmp.v5dhVzl806/repo$ git checkout dev
Previous HEAD position was c2606df initial commit of README.md
Branch 'dev' set up to track remote branch 'dev' from 'origin'.
Switched to a new branch 'dev'
bandit29@bandit:/tmp/tmp.v5dhVzl806/repo$ git log -p -1
commit fbbce0ec6c80acb0fdc00ebb4b5228dd868fd799 (HEAD -> dev, origin/dev)
Author: Morla Porla <morla@overthewire.org>
Date:   Tue Feb 21 22:03:11 2023 +0000

    add data needed for development

diff --git a/README.md b/README.md
index 1af21d3..a4b1cf1 100644
--- a/README.md
+++ b/README.md
@@ -4,5 +4,5 @@ Some notes for bandit30 of bandit.
 ## credentials

 - username: bandit30
-- password: <no passwords in production!>
+- password: xbhV3HpNGlTIdnjUrdAlPzc2L6y9EOnS

bandit29@bandit:/tmp/tmp.v5dhVzl806/repo$
```

## Notas adicionales
| comando | descripción |
| ------ | ------ |
| xx | xx |

## Referencias
- []()