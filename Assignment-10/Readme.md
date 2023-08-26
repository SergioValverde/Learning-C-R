ssignment 10

Create an integer array with 10 integers and then print the number of elements in the array to the terminal.

Hint: Play with the sizeof() function to determine how many bytes of storage an integer takes up.

Example
```
tokyo:~/LearningC/ # ./assignment10                                 
The array has 10 elements.#   
```
------

###CODE

```
# include <stdio.h>


int main(void) {

	int i;
	int n[10];// = { 1,1,1,1,1,1,1,1,1,1 };
	
	
	n[0] = 5;
	n[1] = 15;
	n[2] = 115;
	n[3] = 1115;
	n[4] = 11115;
	n[5] = 111115;
	n[6] = 1111115;
	n[7] = 11111115;
	n[8] = 111111115;
	n[9] = 1111111115;
	
	
	for (i = 0; i < 10; i++) {

		printf("The array has %d\n", n[i]);

	}
	printf("el valor del array es %d\n", sizeof(n));

	int elements = (sizeof(n) / 4);

	printf("el número de elementos totaltes es es %d\n", elements);
	
	return 0;
}
```
