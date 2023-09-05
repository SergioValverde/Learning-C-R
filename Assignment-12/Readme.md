Assignment 12

Prompt the user for a number of coin flips (x) and then simulate (x) number of coin flips and print the results to the terminal.

Hint: Look up the srand() function.
Example Output
```
tokyo:~/LearningC/ # ./assignment12                                  
How many times would you like to flip the coin? 5000
After flipping the coin 5000 times, the results were
2536 heads
2464 tails
```
------

### CODE

```
#include <stdio.h>
#include <stdlib.h>
#include <time.h>

int main(void) {
	
	unsigned int flip;
	//unsigned int random;
	

	// Seed the random number generator with the current time
	srand((unsigned int)time(NULL));


	printf("How many times would you like to flip the coin?\n");

	scanf_s("%u", &flip);
	
	if (!flip) {
		printf("Enter a positive number");
		return 1;
	}
	
	
	int tails = 0;
	int heads = 0;
	

	for (int i = 0; i < flip; i++) {

		int result = rand() % 2;

		if (result == 1) {
			heads++;
		}
		else  {
			tails++;
		}

	}
	
	printf("Heads: %d\n", heads);
	printf("Tails: %d\n", tails);

	return 0;

}
```
