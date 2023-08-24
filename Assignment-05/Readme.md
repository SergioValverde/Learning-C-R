Assignment 5

Prompt the user for a number of seconds. Take the user's input and convert the number of seconds into its duration in Hours, Minutes, and remaining Seconds.

Extra Credit: Make sure the Hours, Minutes, and Seconds print with no decimal places.
Example Output

tokyo:~/LearningC/ # ./assignment5                                        
Enter the amount of seconds: 18550
18550 seconds is equal to 5 hours, 9 minutes, and 10 seconds.#

### CODE


```
#include <stdio.h>


int main()
{
	float nseconds, seconds, minutes, hours;

	printf("Introduce el número de seconds:\n ");
	scanf_s("%f", &nseconds);

	hours = (int)(nseconds / 3600);

	minutes = (int)((nseconds - (hours * 3600))/60);

	seconds = (nseconds - (hours * 3600) - (minutes * 60));


	printf("El nº de segundos equivale a %0.0f, %0.0f, %0.0f es igual a ", hours, minutes, seconds);
	
}
```
