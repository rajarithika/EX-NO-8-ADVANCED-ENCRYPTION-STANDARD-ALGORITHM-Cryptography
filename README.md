# EX-NO-8-ADVANCED-ENCRYPTION-STANDARD-ALGORITHM


## Aim:
To use Advanced Encryption Standard (AES) Algorithm for a practical application like URL Encryption.

## ALGORITHM:

1.AES is based on a design principle known as a substitution–permutation.

2.AES does not use a Feistel network like DES, it uses variant of Rijndael.

3.It has a fixed block size of 128 bits, and a key size of 128, 192, or 256 bits.

4.AES operates on a 4 × 4 column-major order array of bytes, termed the state

## PROGRAM:
```
#include <stdio.h>
#include <string.h>

void xor_fun(char *a, char *k) {
    int i;
    for(i=0;i<strlen(a);i++)
        a[i] = a[i] ^ k[i % strlen(k)];
}

int main() {
    char url[] = "Bhoopesh";
    char key[] = "megu";

    printf("Original: %s\n", url);

    xor_fun(url, key);

    printf("Encrypted: ");
    for(int i=0;i<strlen(url);i++)
        printf("%02X ", (unsigned char)url[i]);

    printf("\n");

    xor_fun(url, key);
    printf("Decrypted: %s\n", url);

    return 0;
}
```
## OUTPUT:

<img width="557" height="299" alt="image" src="https://github.com/user-attachments/assets/b8073bcc-22d0-4c6b-b406-37dd32541503" />


## RESULT:

Hence the experiment has been executed successfully
