# Nombre

# Objetivo
What can you do with this file? I forgot the key to my safe but this [file](https://artifacts.picoctf.net/c/290/SafeOpener.class) is supposed to help me with retrieving the lost key. Can you help me unlock my safe?

# Pistas
- Download and try to decompile the file.

# Solución
- Descargamos el archivo
- Le hacemos un strings
```
jesjua-picoctf@webshell:~$ strings SafeOpener.class | grep "picoCTF"
,picoCTF{SAf3_0p3n3rr_y0u_solv3d_it_7db9fb8c}
jesjua-picoctf@webshell:~$
```

Solución 2:
- Descargamos el archivo
- Entramos a una [pagina para descompilar](http://www.javadecompilers.com/) el archivo .class para volverlo a un .java
- Archivo resultante al descompilar
```
import java.io.IOException;
import java.util.Base64;
import java.io.Reader;
import java.io.BufferedReader;
import java.io.InputStreamReader;

// // Decompiled by Procyon v0.5.36
// public class SafeOpener
{
    public static void main(final String[] args) throws IOException {
        final BufferedReader keyboard = new BufferedReader(new InputStreamReader(System.in));
        final Base64.Encoder encoder = Base64.getEncoder();
        String encodedkey = "";
        String key = "";
        for (int i = 0; i < 3; ++i) {
            System.out.print("Enter password for the safe: ");
            key = keyboard.readLine();
            encodedkey = encoder.encodeToString(key.getBytes());
            System.out.println(encodedkey);
            final boolean isOpen = openSafe(encodedkey);
            if (isOpen) {
                break;
            }
            System.out.println("You have  " + (2 - i) + " attempt(s) left");
        }
    }
    
    public static boolean openSafe(final String password) {
        final String encodedkey = "picoCTF{SAf3_0p3n3rr_y0u_solv3d_it_7db9fb8c}";
        if (password.equals(encodedkey)) {
            System.out.println("Sesame open");
            return true;
        }
        System.out.println("Password is incorrect\n");
        return false;
    }
}
```

# Bandera
picoCTF{SAf3_0p3n3rr_y0u_solv3d_it_7db9fb8c}

## Notas adicionales
| comando | descripción |
| ------ | ------ |
| xx | xx |

## Referencias
- []()