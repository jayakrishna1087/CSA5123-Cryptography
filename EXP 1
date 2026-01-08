#include <stdio.h>
#include <ctype.h>
#include <string.h>

void encrypt(char* message, int key) {
    for (int i = 0; message[i] != '\0'; ++i) {
        char ch = message[i];

        if (isalpha(ch)) {
            char base = islower(ch) ? 'a' : 'A';
            ch = (ch - base + key) % 26 + base;
        }

        message[i] = ch;
    }
}

int main() {
    char message[1000];
    int key;

    printf("Enter a message: ");
    fgets(message, sizeof(message), stdin);

    printf("Enter key (1-25): ");
    scanf("%d", &key);

    if (key < 1 || key > 25) {
        printf("Invalid key! Must be between 1 and 25.\n");
        return 1;
    }

    encrypt(message, key);

    printf("Encrypted message: %s\n", message);

    return 0;
}
