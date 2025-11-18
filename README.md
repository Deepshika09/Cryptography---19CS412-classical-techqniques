
# Rail Fence Cipher
Rail Fence Cipher using with different key values

# AIM:

To develop a simple C program to implement Rail Fence Cipher.

## DESIGN STEPS:

### Step 1:

Design of Rail Fence Cipher algorithnm 

### Step 2:

Implementation using C or pyhton code

### Step 3:

Testing algorithm with different key values. 
ALGORITHM DESCRIPTION:
In the rail fence cipher, the plaintext is written downwards and diagonally on successive "rails" of an imaginary fence, then moving up when we reach the bottom rail. When we reach the top rail, the message is written downwards again until the whole plaintext is written out. The message is then read off in rows.

## PROGRAM:

PROGRAM:
```
#include <stdio.h>
#include <string.h>
#include <ctype.h>
void encryptRailFence(char *message, int rails) {
int len = strlen(message);
char rail[rails][len];
memset(rail, '\n', sizeof(rail));
int row = 0, direction = 1;
for (int i = 0; i < len; i++) {
rail[row][i] = message[i];
row += direction;
if (row == rails- 1 | row == 0)
direction =-direction;
}
printf("Encrypted text: ");
for (int i = 0; i < rails; i++)
for (int j = 0; j < len; j++)
if (rail[i][j] != '\n')
printf("%c", rail[i][j]);
printf("\n");
}
int main() {
char message[100];
int rails;
printf("Enter a Secret Message: ");
scanf("%s", message);
printf("Enter number of rails: ");
scanf("%d", &rails);
encryptRailFence(message, rails);
return 0;
}
```

## OUTPUT:

<img width="556" height="249" alt="Screenshot 2025-11-18 152137" src="https://github.com/user-attachments/assets/962e9d4c-ab33-425e-a075-f91d20a2c301" />


## RESULT:
The program is executed successfully
