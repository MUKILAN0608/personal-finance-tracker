#include <stdio.h>
#include <string.h>
#define MAX_EXPENSES 100
#define DESCRIPTION_LENGTH 50




struct Expense {
    char description[200];
    float amount;
};


void addExpense(struct Expense expenses[], int *count) {
    if (*count >= MAX_EXPENSES) {
        printf("Expense limit reached. Cannot add more expenses.\n");
        return;
    }

    struct Expense newExpense;

    printf("Enter description for the expense: ");
    scanf("%s", newExpense.description);

    printf("Enter amount: ");
    scanf("%f", &newExpense.amount);

    expenses[*count] = newExpense;
    (*count)++;

    printf("Expense added successfully.\n");
}

// Function to display all expenses
void displayExpenses(struct Expense expenses[], int count) {
    if (count == 0) {
        printf("No expenses to display.\n");
        return;
    }

    printf("Expenses:\n");
    for (int i = 0; i < count; i++) {
        printf("%d. Description: %s, Amount: $%.2f\n", i + 1, expenses[i].description, expenses[i].amount);
    }
}

int main() {
    struct Expense expenses[MAX_EXPENSES];
    int count = 0;
    int choice;

    do {
        printf("\nPersonal Finance Tracker\n");
        printf("1. Add Expense\n");
        printf("2. Display Expenses\n");
        printf("3. Exit\n");
        printf("Enter your choice: ");
        scanf("%d", &choice);

        switch (choice) {
            case 1:
                addExpense(expenses, &count);
                break;
            case 2:
                displayExpenses(expenses, count);
                break;
            case 3:
                printf("Exiting program.\n");
                break;
            default:
                printf("Invalid choice. Please enter a valid option.\n");
        }
    } while (choice != 3);

    return 0;
}
