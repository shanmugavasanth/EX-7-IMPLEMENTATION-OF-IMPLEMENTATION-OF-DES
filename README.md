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

## OUTPUT:

## Result:
The program implementing the Data Encryption Standard (DES) for encryption and decryption	has	been	successfully	executed,	and	the	results	have	been	verified.
