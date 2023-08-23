
Assignment 3

Prompt the user to input their first and last name and then print them a welcome message. Try storing the input as a char variable's value.

Easy Mode: Allocate an arbitrary amount of indices to your char array and pray to the gods that the user input fits.

Extra Credit: Dynamically allocate the array size of your char variable based on the length of the user's input.
Example Output
-----
```
tokyo:~/LearningC/ # ./assignment3                                     
Enter your first name: Jimmy
Enter your last name: Smith
Hello Jimmy Smith!
```

------

###Code

```
int main() {
	char name[10];
	char lastname[10];

	printf("Introduce tu nombre:\n ");
	scanf("%s", name);

	printf("Introduce tu apellido:\n ");
	scanf("%s", lastname);

	printf("Welcome %s, %s" name, lastname);

	return 0;
}
```
