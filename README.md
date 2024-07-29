
# Substitution Cipher Program

## Overview

This program implements a substitution cipher, which is a method of encryption where each letter in the plaintext is replaced with another letter from a fixed substitution alphabet. This implementation is part of the CS50 course assignment, focusing on creating a secure cipher based on user-provided keys.

## Features

- Key Validation: Checks if the provided key has exactly 26 characters and contains only alphabetic characters.
- Uniqueness Check: Ensures that each letter in the key is unique.
- Encryption: Transforms plaintext input into ciphertext using the provided key.

## Usage

1. Compile the Program:
  
   make substitution
   
2. Run the Program:
  
   ./substitution <key>
   
   Replace <key> with a 26-character substitution key. The key must contain each letter of the alphabet exactly once.

3. Input Plaintext:
   After running the program, you will be prompted to enter plaintext. The program will output the corresponding ciphertext based on the provided key.

## Example

To encrypt the message "In love with some one" with the key "BCDEFGHIJKLMNOPQRSTUVWXYZA":

./substitution BCDEFGHIJKLMNOPQRSTUVWXYZA
You will then enter the plaintext:

In love with some one
The program will output the ciphertext:

Jo mpwf xjui tpnf pof
## Code Explanation

- Key Validation:
  - Checks if the key length is 26 characters.
  - Validates that the key contains only alphabetic characters.
  - Ensures that no characters are repeated in the key.

- Cipher Function:
  - Converts each letter of the plaintext to its corresponding letter in the cipher key.
  - Keeps non-alphabetic characters unchanged.

## License

This project is licensed under the MIT License. See the LICENSE file for details.

## Author

[Ye Yint Aung]
