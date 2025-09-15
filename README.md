## EX 7 : IMPLEMENTATION OF IMPLEMENTATION OF DES

## AIM:

To implement the working of the Data Encryption Standard (DES) using a simplified XOR-based encryption and decryption method in C programming.

## ALGORITHM:
To Perform Encryption:
1.	Start the program.
2.	Accept the plaintext message and encryption key from the user.
3.	Calculate the length of the message.
4.	For each character in the message:
•	XOR the character with the corresponding character in the key.
•	If the key is shorter than the message, repeat the key using key[i % keyLength].
•	Store the result in the encrypted message array.
5.	Null-terminate the encrypted message string.
6.	Display the encrypted message in hexadecimal format.
To Perform Decryption:
7.	For each character in the encrypted message:
•	XOR it with the same corresponding character from the key.
•	This reverses the XOR operation, retrieving the original character.
8.	Null-terminate the decrypted message string.
9.	Display the decrypted message.
10.	End the program.


## PROGRAM:
```
#include <stdio.h>
#include <string.h>

int main() {
    char message[256], key[256], encrypted[256], decrypted[256];
    int i, msgLen, keyLen;

    printf("Enter the plaintext message: ");
    fgets(message, sizeof(message), stdin);
    message[strcspn(message, "\n")] = '\0';

    printf("Enter the key: ");
    fgets(key, sizeof(key), stdin);
    key[strcspn(key, "\n")] = '\0';

    msgLen = strlen(message);
    keyLen = strlen(key);

    for (i = 0; i < msgLen; i++)
        encrypted[i] = message[i] ^ key[i % keyLen];
    encrypted[msgLen] = '\0';

    printf("\nEncrypted message (in hex): ");
    for (i = 0; i < msgLen; i++)
        printf("%02X ", (unsigned char)encrypted[i]);

    for (i = 0; i < msgLen; i++)
        decrypted[i] = encrypted[i] ^ key[i % keyLen];
    decrypted[msgLen] = '\0';

    printf("\nDecrypted message: %s\n", decrypted);

    return 0;
}
```
## OUTPUT:

<img width="480" height="126" alt="Screenshot 2025-09-15 135750" src="https://github.com/user-attachments/assets/60626578-3da8-4616-ac2d-634f56a644ce" />


## Result:
The program implementing the Data Encryption Standard (DES) for encryption and decryption	has	been	successfully	executed,	and	the	results	have	been	verified.
