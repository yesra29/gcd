# gcd
#include <stdio.h>

// Function to calculate the HCF (GCD) of two numbers
int calculateHCF(int num1, int num2) {
    while (num1 != num2) {
        if (num1 > num2)
            num1 -= num2;
        else
            num2 -= num1;
    }
    return num1;
}

int main() {
    int num1, num2;

    // Get the two numbers from the user
    printf("Enter first number: ");
    scanf("%d", &num1);

    printf("Enter second number: ");
    scanf("%d", &num2);

    // Call the function to calculate and print the HCF
    printf("HCF of %d and %d is %d\n", num1, num2, calculateHCF(num1, num2));

    return 0;
}
