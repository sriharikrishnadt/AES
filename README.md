# EX-8-ADVANCED-ENCRYPTION-STANDARD ALGORITHM
# Aim:
To use Advanced Encryption Standard (AES) Algorithm for a practical application like URL Encryption.

# ALGORITHM:
AES is based on a design principle known as a substitution–permutation.
AES does not use a Feistel network like DES, it uses variant of Rijndael.
It has a fixed block size of 128 bits, and a key size of 128, 192, or 256 bits.
AES operates on a 4 × 4 column-major order array of bytes, termed the state
# PROGRAM:
```
#include <stdio.h>
#include <string.h>

void xorCrypt(char msg[], char key[])
{
    int i, klen = strlen(key);
    for(i = 0; msg[i] != '\0'; i++)
    {
        msg[i] = msg[i] ^ key[i % klen];
    }
}

int main()
{
    char msg[] = "SRI HARI KRISHNA";
    char key[] = "secretkey";

    printf("Original: %s\n", msg);
    xorCrypt(msg, key);
    printf("Encrypted: %s\n", msg);
    xorCrypt(msg, key);
    printf("Decrypted: %s\n", msg);

    return 0;
}
```

# OUTPUT:
<img width="1702" height="539" alt="image" src="https://github.com/user-attachments/assets/fb6c6bae-df1e-4a92-99a5-974972704651" />


# RESULT:
Hence Advanced Encryption Standard (AES) Algorithm for a practical application like URL Encryption is done successfully.


