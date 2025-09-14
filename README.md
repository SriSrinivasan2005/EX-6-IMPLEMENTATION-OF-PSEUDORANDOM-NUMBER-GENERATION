## NAME : SRI SRINIVASAN K
## REGISTER NUMBER : 212224220104
## EX: 6 IMPLEMENTATION OF PSEUDORANDOM NUMBER GENERATION 

## AIM:
To Implement Pseudorandom Number Generation Using Standard library.


## ALGORITHM:

1.	Start the program and import the required libraries.
2.	Seed the random number generator using the current time (i.e) rand(time(0));
3.	Get the number of random numbers to generate.
4.	Pass the value for number of iterations and print the numbers.
5.	End the program.


## PROGRAM:
```
#include <stdio.h>
#include <stdlib.h>
#include <time.h>

int main() {
    int count, min, max;

    // Input: Number of random values
    printf("Enter the number of random numbers to generate: ");
    scanf("%d", &count);

    // Input: Minimum value
    printf("Enter the minimum value: ");
    scanf("%d", &min);

    // Input: Maximum value
    printf("Enter the maximum value: ");
    scanf("%d", &max);

    // Basic input validation
    if (count <= 0 || min > max) {
        printf("Invalid input. Please ensure count > 0 and min <= max.\n");
        return 1;
    }

    // Optional: Notify if all values will be the same
    if (min == max) {
        printf("Note: All generated numbers will be %d.\n", min);
    }

    // Seed the random number generator
    srand(time(NULL));

    printf("\nPseudorandom numbers:\n");

    // Generate and print random numbers
    for (int i = 0; i < count; i++) {
        int random_number = (rand() % (max - min + 1)) + min;
        printf("%d\n", random_number);
    }

    return 0;
}
```
## OUTPUT:
<img width="813" height="468" alt="image" src="https://github.com/user-attachments/assets/90e73e8c-f205-472a-ba6c-6b3fe79a7b92" />

## RESULT:
The Implementation of Pseudorandom Number Generation Using Standard library is successful.
