Assignment 8

Ask the user for a number between 1 and 500 and then display what range that number is in from the following:

    1 - 100
    101 - 200
    201 - 300
    301 - 400
    401 - 500


Output 
```
tokyo:~/LearningC/ # ./assignment8                                                                           
Enter a number between 1 and 500: 50
Your number is between 1 and 100!#
tokyo:~/LearningC/ # ./assignment8                                                                          
Enter a number between 1 and 500: 150
Your number is between 101 and 200!#
tokyo:~/LearningC/ # ./assignment8                                                                         
Enter a number between 1 and 500: 250
Your number is between 201 and 300!#
tokyo:~/LearningC/ # ./assignment8                                                                        
Enter a number between 1 and 500: 350
Your number is between 301 and 400!#
tokyo:~/LearningC/ # ./assignment8                                                                         
Enter a number between 1 and 500: 450
Your number is between 401 and 500!#
tokyo:~/LearningC/ # ./assignment8                                                                            
Enter a number between 1 and 500: 550
Your number was not in any of our ranges.#
```

-----

###CODE

```
#include<stdio.h>

int main(void)
{

	int number;

	printf("Enter a number between 1 and 500:\n");
	scanf_s("%d", &number);

	if (number <= 100) {
		printf("Your number is low than 100\n");
	}
	
	else if (number >= 101 && number <= 200) {
		printf("Your number is between 100 and 200\n");
	}	
	
	else if (number >= 200 && number <= 300) {
		printf("Your number is between 100 and 200\n");
	}
	
	else if (number >= 300 && number <= 400) {
		printf("Your number is between 100 and 200\n");
	}
	
	else if (number >= 400 && number <= 500) {
		printf("Your number is between 100 and 200\n");
	}
	
	if (number >= 500) {
		printf("Your number is bigger than 500");
	}
	return 0;
}
```
