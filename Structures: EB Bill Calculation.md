## Structures: EB Bill Calculation (C Program)
## Aim
Create a C program using a structure to calculate the electricity bill (EB bill) for 3 customers based on their electricity usage.

## Algorithm
Step 1: Input: Read customer number, previous reading, and current reading for 3 customers into an array of structures e.

Step 2: Calculate Bill: Calculate the units consumed by subtracting previous reading from current reading.

Step 3: Apply billing rates:

    First 100 units: ₹2 per unit

    101 to 200 units: ₹3 per unit

    Above 200 units: ₹5 per unit

Step 4:Output: Display customer number and the calculated bill amount for each customer

## Program
```
#include <stdio.h>

struct Customer {
    int cust_no;
    int prev_reading;
    int curr_reading;
    int units;
    int bill_amount;
};

int calculate_bill(int units) {
    int bill = 0;
    if (units <= 100) {
        bill = units * 2;
    } else if (units <= 200) {
        bill = 100 * 2 + (units - 100) * 3;
    } else {
        bill = 100 * 2 + 100 * 3 + (units - 200) * 5;
    }
    return bill;
}

int main() {
    struct Customer e[3];
    int i;

    for (i = 0; i < 3; i++) {
        printf("Enter details for customer %d\n", i + 1);
        printf("Customer number: ");
        scanf("%d", &e[i].cust_no);
        printf("Previous reading: ");
        scanf("%d", &e[i].prev_reading);
        printf("Current reading: ");
        scanf("%d", &e[i].curr_reading);

        e[i].units = e[i].curr_reading - e[i].prev_reading;
        e[i].bill_amount = calculate_bill(e[i].units);
    }

    printf("\nCustomer Number\tBill Amount\n");
    for (i = 0; i < 3; i++) {
        printf("%d\t\t₹%d\n", e[i].cust_no, e[i].bill_amount);
    }

    return 0;
}
```

## Output
Sample Output 1:
Enter details for customer 1
Customer number: 101
Previous reading: 1000
Current reading: 1100
Enter details for customer 2
Customer number: 102
Previous reading: 1500
Current reading: 1700
Enter details for customer 3
Customer number: 103
Previous reading: 2000
Current reading: 2300

Customer Number    Bill Amount
101               ₹200
102               ₹500
103               ₹950


Sample Output 2:
Enter details for customer 1
Customer number: 201
Previous reading: 300
Current reading: 450
Enter details for customer 2
Customer number: 202
Previous reading: 100
Current reading: 250
Enter details for customer 3
Customer number: 203
Previous reading: 400
Current reading: 500

Customer Number    Bill Amount
201               ₹350
202               ₹350
203               ₹250

## Result
Program was implemented and executed.
