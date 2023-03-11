# PW Crack 1

## Descripción
Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/53/level1.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/53/level1.flag.txt.enc) in the same directory too.

## Pistas
- To view the file in the webshell, do: `$ nano level1.py`
- To exit `nano`, press Ctrl and x and follow the on-screen prompts.
- The `str_xor` function does not need to be reverse engineered for this challenge.

## Solución
```bash
jesjua-picoctf@webshell:~$ ls
README.txt  level1.flag.txt.enc  level1.py
jesjua-picoctf@webshell:~$ python3 level1.py 
Please enter correct password for flag: ^CTraceback (most recent call last):
  File "/home/jesjua-picoctf/level1.py", line 28, in <module>
    level_1_pw_check()
  File "/home/jesjua-picoctf/level1.py", line 18, in level_1_pw_check
    user_pw = input("Please enter correct password for flag: ")
KeyboardInterrupt

jesjua-picoctf@webshell:~$ cat level1.
cat: level1.: No such file or directory
jesjua-picoctf@webshell:~$ cat level1.
level1.flag.txt.enc  level1.py            
jesjua-picoctf@webshell:~$ cat level1.flag.txt.enc 
[gE]__TgS^S
jesjua-picoctf@webshell:~$ python3 level1.py 
Please enter correct password for flag: [gE]__TgS^S
That password is incorrect
jesjua-picoctf@webshell:~$ cat level1.py 
### THIS FUNCTION WILL NOT HELP YOU FIND THE FLAG --LT ########################
def str_xor(secret, key):
    #extend key to secret length
    new_key = key
    i = 0
    while len(new_key) < len(secret):
        new_key = new_key + key[i]
        i = (i + 1) % len(key)        
    return "".join([chr(ord(secret_c) ^ ord(new_key_c)) for (secret_c,new_key_c) in zip(secret,new_key)])
###############################################################################


flag_enc = open('level1.flag.txt.enc', 'rb').read()



def level_1_pw_check():
    user_pw = input("Please enter correct password for flag: ")
    if( user_pw == "8713"):
        print("Welcome back... your flag, user:")
        decryption = str_xor(flag_enc.decode(), user_pw)
        print(decryption)
        return
    print("That password is incorrect")



level_1_pw_check()
jesjua-picoctf@webshell:~$ python3 level1.py 
Please enter correct password for flag: 8713
Welcome back... your flag, user:
picoCTF{545h_r1ng1ng_1b2fd683}
jesjua-picoctf@webshell:~$ 
```

## Bandera
picoCTF{545h_r1ng1ng_1b2fd683}

## Notas adicionales
| comando | descripción |
| ------ | ------ |
| xx | xx |

## Referencias
- []()