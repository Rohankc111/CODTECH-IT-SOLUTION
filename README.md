#include <stdio.h>

// Function prototypes
void celsiusToFahrenheit(double celsius);
void celsiusToKelvin(double celsius);
void fahrenheitToCelsius(double fahrenheit);
void fahrenheitToKelvin(double fahrenheit);
void kelvinToCelsius(double kelvin);
void kelvinToFahrenheit(double kelvin);

int main() {
    int choice;
    double temp;

    while (1) {
        // Display menu
        printf("Temperature Conversion Menu:\n");
        printf("1. Celsius to Fahrenheit\n");
        printf("2. Celsius to Kelvin\n");
        printf("3. Fahrenheit to Celsius\n");
        printf("4. Fahrenheit to Kelvin\n");
        printf("5. Kelvin to Celsius\n");
        printf("6. Kelvin to Fahrenheit\n");
        printf("7. Exit\n");
        printf("Enter your choice (1-7): ");
        scanf("%d", &choice);

        if (choice == 7) {
            printf("Exiting program.\n");
            break;
        }

        if (choice < 1 || choice > 7) {
            printf("Invalid choice. Please enter a number between 1 and 7.\n");
            continue;
        }

        printf("Enter the temperature: ");
        scanf("%lf", &temp);

        // Perform conversion based on user's choice
        switch (choice) {
            case 1:
                celsiusToFahrenheit(temp);
                break;
            case 2:
                celsiusToKelvin(temp);
                break;
            case 3:
                fahrenheitToCelsius(temp);
                break;
            case 4:
                fahrenheitToKelvin(temp);
                break;
            case 5:
                kelvinToCelsius(temp);
                break;
            case 6:
                kelvinToFahrenheit(temp);
                break;
        }
    }

    return 0;
}

// Convert Celsius to Fahrenheit
void celsiusToFahrenheit(double celsius) {
    double fahrenheit = (celsius * 9/5) + 32;
    printf("%.2f Celsius is %.2f Fahrenheit\n", celsius, fahrenheit);
}

// Convert Celsius to Kelvin
void celsiusToKelvin(double celsius) {
    double kelvin = celsius + 273.15;
    printf("%.2f Celsius is %.2f Kelvin\n", celsius, kelvin);
}

// Convert Fahrenheit to Celsius
void fahrenheitToCelsius(double fahrenheit) {
    double celsius = (fahrenheit - 32) * 5/9;
    printf("%.2f Fahrenheit is %.2f Celsius\n", fahrenheit, celsius);
}

// Convert Fahrenheit to Kelvin
void fahrenheitToKelvin(double fahrenheit) {
    double kelvin = (fahrenheit - 32) * 5/9 + 273.15;
    printf("%.2f Fahrenheit is %.2f Kelvin\n", fahrenheit, kelvin);
}

// Convert Kelvin to Celsius
void kelvinToCelsius(double kelvin) {
    double celsius = kelvin - 273.15;
    printf("%.2f Kelvin is %.2f Celsius\n", kelvin, celsius);
}

// Convert Kelvin to Fahrenheit
void kelvinToFahrenheit(double kelvin) {
    double fahrenheit = (kelvin - 273.15) * 9/5 + 32;
    printf("%.2f Kelvin is %.2f Fahrenheit\n", kelvin, fahrenheit);
}
