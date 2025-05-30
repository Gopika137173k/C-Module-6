## Structures: Student Information Storage (C Program)
## Aim
Create a C program to store and display the information of 5 students using an array of structures.

## Algorithm
1. Input: Read the name and marks of 5 students into an array of structures s.

2. Display Information:

    Iterate through the array and print the roll number, name, and marks for each student.

3.End the program execution.

## Program
```
#include <stdio.h>

struct Student {
    int roll_no;
    char name[50];
    int marks;
};

int main() {
    struct Student s[5];
    int i;
    for (i = 0; i < 5; i++) {
        printf("Enter details for student %d\n", i + 1);
        printf("Roll Number: ");
        scanf("%d", &s[i].roll_no);
        printf("Name: ");
        scanf(" %[^\n]", s[i].name);
        printf("Marks: ");
        scanf("%d", &s[i].marks);
    }
    printf("\nStudent Details:\n");
    printf("Roll No\tName\t\tMarks\n");
    for (i = 0; i < 5; i++) {
        printf("%d\t%s\t\t%d\n", s[i].roll_no, s[i].name, s[i].marks);
    }
    return 0;
}
```


## Output
Sample Output 1:
Enter details for student 1
Roll Number: 1
Name: Alice
Marks: 95
Enter details for student 2
Roll Number: 2
Name: Bob
Marks: 88
Enter details for student 3
Roll Number: 3
Name: Charlie
Marks: 76
Enter details for student 4
Roll Number: 4
Name: Diana
Marks: 85
Enter details for student 5
Roll Number: 5
Name: Ethan
Marks: 90

Student Details:
Roll No Name            Marks
1       Alice           95
2       Bob             88
3       Charlie         76
4       Diana           85
5       Ethan           90


Sample Output 2:
Enter details for student 1
Roll Number: 101
Name: John Doe
Marks: 80
Enter details for student 2
Roll Number: 102
Name: Jane Smith
Marks: 85
Enter details for student 3
Roll Number: 103
Name: Mike Brown
Marks: 78
Enter details for student 4
Roll Number: 104
Name: Anna White
Marks: 92
Enter details for student 5
Roll Number: 105
Name: Tom Clark
Marks: 88

Student Details:
Roll No Name            Marks
101     John Doe        80
102     Jane Smith      85
103     Mike Brown      78
104     Anna White      92
105     Tom Clark       88

## Result
Program was implemented and executed.

