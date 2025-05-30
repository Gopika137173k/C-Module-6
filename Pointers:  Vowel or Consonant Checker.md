# # Pointers: Vowel or Consonant Checker Using Pointers in C

## 🎯 Aim

To write a C program to determine whether a character is a vowel or a consonant using a pointer.

## 🧠 Algorithm

1. **Input**:
   - Read a character from the user.
   - Store the character's address in a pointer variable `pch`.

2. **Check Vowel**:
   - Use an `if` or `switch` statement to check if the character pointed to by `pch` is one of the vowels: `'A'`, `'E'`, `'I'`, `'O'`, `'U'` (uppercase only).
   - If it matches any of these, it is a **vowel**.
   - Otherwise, it is a **consonant**.

3. **Output**:
   - Print whether the input character is a vowel or consonant.

## Program
```
#include <stdio.h>

int main() {
    char ch, *pch;

    printf("Enter a character (uppercase A-Z): ");
    scanf("%c", &ch);

    pch = &ch;

    if (*pch == 'A' || *pch == 'E' || *pch == 'I' || *pch == 'O' || *pch == 'U') {
        printf("%c is a vowel.\n", *pch);
    } else {
        printf("%c is a consonant.\n", *pch);
    }

    return 0;
}
```

## Output
Sample Output 1:
Enter a character (uppercase A-Z): A
A is a vowel.

Sample Output 2:
Enter a character (uppercase A-Z): B
B is a consonant.


## Result
Program was implemented and executed.
