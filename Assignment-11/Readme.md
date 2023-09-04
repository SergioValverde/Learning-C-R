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

###CODE 

```
#include <stdio.h>

int main(void) {
	
	int value[10];
	int i=0;
	char answer[] = "Y";
	char N = 'N';



	
	while (strcmp(answer, "Y") == 0) {
		
		printf("Enter a test score:\n");

		scanf_s("%d", &value[i]);

		//increase our counter
		i++;


		printf("Would you like to continue? Y/N");

		scanf_s("%s", &answer);

		

	}

	int loop;
	int sum = 0;

	//start a loop that will start at 0, and then it'll iterate through our scores array until it reaches the end
	//each element in the array will be added to the sum so that we can find the average
	for (loop = 0; loop < i; loop++)
	{
		sum = sum + value[loop];
	}

	//do the maths
	float average;

	average = (float)sum / loop;

	printf("%.2f is the average.\n", average);
}
```

