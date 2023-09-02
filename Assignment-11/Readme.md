Assignment 11

Ask the user for test scores and then keep asking the user if they would like to continue or end the program. Store all test score values and calculate an average score that prints to the terminal when the user ends the program. You can initialize your array size as 10 and let's use a max test score count of 8 for this.

Print the average of the test scores to the second decimal place.

Hint: Look up while and for loops. Look up the strcmp() function.

Example

```
tokyo:~/LearningC/ # ./assignment11                                 
Enter a test score: 97
Would you like to continue? Y/N Y
Enter a test score: 86
Would you like to continue? Y/N Y
Enter a test score: 82
Would you like to continue? Y/N Y
Enter a test score: 91
Would you like to continue? Y/N Y
Enter a test score: 66
Would you like to continue? Y/N Y
Enter a test score: 99
Would you like to continue? Y/N N
86.83 is the average.
```

------

###CODE - NO Funciona

```
#include <stdio.h>


int main() {
    float x[10];
    int i = 0;
    
    char answer[] = "Y";

    //v = getchar();

    while (strcmp(answer, "Y") == 0) {
        
        printf("Enter a test score:\n");
        scanf_s("%f", &x[i]);

        i++;


        printf("Would you like to continue ? Y / N\n");
        scanf_s("%1s", &answer);

    }
    
      return 0;
}
```

