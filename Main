#include <cs50.h>
#include <ctype.h>
#include <stdio.h>
#include <stdlib.h>
#include <string.h>

bool it_alpha = true;      // Store bool value of it alpha or not
bool it_not_repeat = true; // Store bool value of it have repeat char or not
bool len = true;           // Store bool value of it have 26 characters

void lenCheck(string K0);
void alphCheck(string K1);
void charCheck(string K2);
void cipher(string K3, string user_input, char *ciphertext);

int main(int argc, string argv[])
{
    if (argc != 2)
    {
        printf("Usage: ./substitution key\n");
        return 1;
    }

    string key = argv[1];

    lenCheck(key);  // length check
    alphCheck(key); // alphabet check
    charCheck(key); // Character check

    if (!len || !it_not_repeat || !it_alpha)
    {
        return 1;
    }

    string U_input = get_string("plaintext: ");

    char *ciphertext = malloc((strlen(U_input) + 1) * sizeof(char));

    if (ciphertext == NULL)
    {
        printf("Memory allocation failed\n");
        return 1;
    }

    cipher(key, U_input, ciphertext);

    printf("ciphertext: %s\n", ciphertext);

    free(ciphertext);

    return 0;
}

// check length
void lenCheck(string K0)
{
    int key_len = strlen(K0); // check for string length
    if (key_len != 26)
    {
        printf("Key must contain 26 charcters.\n");
        len = false;
    }
    else
    {
        len = true;
    }
}

// Check Key
void alphCheck(string K1)
{
    for (int i = 0; i < strlen(K1); i++)
    {
        if (!isalpha(K1[i]))
        {
            printf("Key should only conatin alphabet!\n");
            it_alpha = false;
        }
    }
}

// check for aphabet repeat or not in key
void charCheck(string K2)
{
    for (int i = 0; i < strlen(K2); i++)
    {
        for (int j = i + 1; j < strlen(K2); j++)
        {
            if (K2[i] == K2[j])
            {
                printf("Key should only containing each letter exactly once!\n");
                it_not_repeat = false;
            }
        }
    }
}

void cipher(string K3, string user_input, char *ciphertext)
{
    int leng = strlen(user_input);
    for (int i = 0; i < strlen(user_input); i++)
    {
        if (isupper(user_input[i]))
        {
            char E = K3[user_input[i] - 'A'];
            ciphertext[i] = toupper(E); // to change key in upper case
        }
        else if (islower(user_input[i]))
        {
            char T = K3[user_input[i] - 'a'];
            ciphertext[i] = tolower(T); // to change key in lower case
        }
        else
        {
            ciphertext[i] = user_input[i];
        }
    }
    ciphertext[leng] = '\0';
}
