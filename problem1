#include <stdio.h>

void displayMenu();
void handleTransaction();

int main() {
    handleTransaction();
    return 0;
}

void displayMenu() {
    printf("MENU\n");
    printf("1. Deposit Money\n");
    printf("2. Withdraw Money\n");
    printf("3. Check Balance\n");
    printf("4. Exit\n");
}

void handleTransaction() {
    int choice;
    double balance = 0.0, amount;

    while (1) {
        displayMenu();
        printf("Enter your choice (1-4): ");
        
        if (scanf("%d", &choice) != 1) {
            printf("Invalid input! Please enter a number between 1 and 4.\n");
            while (getchar() != '\n'); // Clear input buffer
            continue;
        }

        if (choice == 4) {
            printf("Exiting.\n");
            break;
        }

        switch (choice) {
            case 1:
                printf("Enter amount to deposit: ");
                if (scanf("%lf", &amount) != 1 || amount <= 0) {
                    printf("Invalid amount! Please enter a positive value.\n");
                    while (getchar() != '\n'); // Clear input buffer
                } else {
                    balance += amount;
                    printf("Successfully deposited: %.2lf\n", amount);
                }
                break;

            case 2:
                printf("Enter amount to withdraw: ");
                if (scanf("%lf", &amount) != 1 || amount <= 0) {
                    printf("Invalid amount! Please enter a positive value.\n");
                    while (getchar() != '\n'); // Clear input buffer
                } else if (amount > balance) {
                    printf("Insufficient funds! Available balance: %.2lf\n", balance);
                } else {
                    balance -= amount;
                    printf("Successfully withdrew: %.2lf\n", amount);
                }
                break;

            case 3:
                printf("Your current balance: %.2lf\n", balance);
                break;

            default:
                printf("Invalid choice! Please enter a number between 1 and 4.\n");
        }
    }
}
