#include <stdio.h>

int main() {
    int choice, qty;
    float total = 0;

    while (1) {
        printf("\n====== HOTEL MENU ======\n");
        printf("1. Pizza       - Rs 120\n");
        printf("2. Burger      - Rs 80\n");
        printf("3. Sandwich    - Rs 70\n");
        printf("4. Coffee      - Rs 50\n");
        printf("5. Exit\n");

        printf("Enter your choice: ");
        scanf("%d", &choice);

        if (choice == 5) {
            break;
        }

        printf("Enter quantity: ");
        scanf("%d", &qty);

        switch (choice) {
            case 1:
                total += 120 * qty;
                break;
            case 2:
                total += 80 * qty;
                break;
            case 3:
                total += 70 * qty;
                break;
            case 4:
                total += 50 * qty;
                break;
            default:
                printf("Invalid choice!\n");
        }
    }

    printf("\n====== BILL ======\n");
    printf("Total amount: Rs %.2f\n", total);
    printf("Thank you! Visit again 😊\n");

    return 0;
}
