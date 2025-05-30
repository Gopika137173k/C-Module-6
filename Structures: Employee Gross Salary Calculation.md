## Structures: Employee Gross Salary Calculation (C Program)
## Aim
Write a C program to read and store the data of 3 employees and calculate their Gross Salary using the concept of structures.

## Algorithm
Step 1: Start the program.

Step 2: Create a structure employee with members: name, id, and salary.

Step 3: Input: Using a structure array, read the name, ID, and basic salary for 3 employees.

Step 4: Calculate: Compute the Gross Salary based on a predefined formula (e.g., adding allowances like DA, HRA, etc., if applicable) or by using basic salary as gross salary if no formula is given.

Step 5: Output: Display employee details including name, ID, and calculated Gross Salary.

Step 6: Stop the program.

## Program 
```
#include <stdio.h>

struct Employee {
    char name[50];
    int id;
    float basic_salary;
    float gross_salary;
};

int main() {
    struct Employee emp[3];
    int i;
    float DA, HRA;

    for (i = 0; i < 3; i++) {
        printf("Enter details for employee %d\n", i + 1);

        printf("Name: ");
        scanf(" %[^\n]", emp[i].name);

        printf("ID: ");
        scanf("%d", &emp[i].id);

        printf("Basic Salary: ");
        scanf("%f", &emp[i].basic_salary);

        DA = 0.10 * emp[i].basic_salary;
        HRA = 0.05 * emp[i].basic_salary;
        emp[i].gross_salary = emp[i].basic_salary + DA + HRA;
    }

    printf("\nEmployee Details:\n");
    printf("Name\t\tID\tGross Salary\n");
    for (i = 0; i < 3; i++) {
        printf("%s\t%d\t%.2f\n", emp[i].name, emp[i].id, emp[i].gross_salary);
    }

    return 0;
}
```


## Output
Sample Output 1:
Enter details for employee 1
Name: John Doe
ID: 201
Basic Salary: 25000
Enter details for employee 2
Name: Jane Smith
ID: 202
Basic Salary: 30000
Enter details for employee 3
Name: Mike Brown
ID: 203
Basic Salary: 28000

Employee Details:
Name            ID      Gross Salary
John Doe        201     28750.00
Jane Smith      202     34500.00
Mike Brown      203     32200.00


Sample Output 2:
Enter details for employee 1
Name: Alice Cooper
ID: 301
Basic Salary: 18000
Enter details for employee 2
Name: Bob Marley
ID: 302
Basic Salary: 22000
Enter details for employee 3
Name: Clara Oswald
ID: 303
Basic Salary: 20000

Employee Details:
Name            ID      Gross Salary
Alice Cooper    301     20700.00
Bob Marley      302     25300.00
Clara Oswald    303     23000.00

## Result
Program was implemented and executed.
