# File-Encryption-and-File-Decryption
#file encryption/file decryption
Generating a Key
To encrypt and decrypt files, we need to generate a key that will be used to encrypt and decrypt the data. To generate the key, we will use the Fernet class from the cryptography package.
The generate_key() function generates a key and saves it to a file named secret.key. We are using the with statement to ensure that the file is properly closed after the key is written.

Loading the Key
Now that we have generated the key, we need to load it to use it for encryption and decryption.
The load_key() function opens the secret.key file and returns its contents.

Encrypting the File
The encrypt() function takes two parameters: the filename of the file to encrypt and the key used to encrypt it. First, we create a Fernet object with the key. Then, we open the file in binary mode and read its contents. We then use the encrypt() method of the Fernet object to encrypt the file data. Finally, we write the encrypted data back to the same file.

Decrypting a File
To decrypt a file, we need to load the key from the secret.key file and use it to decrypt the contents of the encrypted file.
The decrypt() function takes two arguments: the filename of the encrypted file and the key to decrypt it. First, we create a Fernet object using the key. Then, we open the encrypted file in binary mode and read its contents. We then use the decrypt() method of the Fernet object to decrypt the contents of the file. If the key is invalid or the file has been tampered with, we catch the Invalid Token exception and print an error message. Otherwise, we write the decrypted contents to the same file.

Putting it All Together
Now that we have implemented the generate_key(), load_key(), encrypt(), and decrypt() functions, we can use them to encrypt and decrypt files. We first ask the user whether they want to encrypt or decrypt a file, and then prompt them for the filename. We then call the appropriate function based on the user's choice.

It is designed to help protect sensitive files by converting them into secure, unreadable formats and restoring them when needed.
