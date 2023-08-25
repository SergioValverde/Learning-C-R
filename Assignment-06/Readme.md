Assignment 6

Prompt the user for a Numerator (top number of a fraction) and a Denominator (bottom number of a fraction). Tell the user whether or not there is a remainder using if control flow.
Example

```
tokyo:~/LearningC/ # ./assignment6                                                                             
Enter a numerator: 24
Enter a denominator: 8
There is NOT a remainder!#
tokyo:~/LearningC/ # ./assignment6                                                                             
Enter a numerator: 55
Enter a denominator: 9
There is a remainder!# 
```
-----

###CODE

```
#include <stdio.h>


int main() {
    
    int Numerator, Denominator, Remainder;

    printf("Introduce el Numerator\n ");
    scanf_s("%d", &Numerator);

    printf("Introduce el Denominator\n ");
    scanf_s("%d", &Denominator);

    Remainder = (Numerator%Denominator);

    if (Remainder == 0) {
            printf("El resto es igual a 0");
    }
    else {
        printf("El resto no es igual a 0");
    }
}
```
