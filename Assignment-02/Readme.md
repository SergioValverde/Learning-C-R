#### Assignment 2

Initialize and assign a value to an integer, float, and char variable. Then print each one with a sentence on a new line describing variable data type.
Example Output
```
tokyo:~/LearningC/ # ./assignment2                                      
5 is an integer!
3.140000 is a float!
Hello, World! is a char!

```

------

Code:


```
#include <stdio.h>

main()
{
	int variable1 = 5;
	float variable2 = 3.14000;
	char variable3[] = "Hello, Wold!";

	printf("%d is an integer!\n", variable1);
	printf("%f is a float!\n", variable2);
	printf("%s is an string!\n", variable3);
}
```







Learnings:

```
%c = char (only one letter)

Leave instruction:
The last instruction LEAVE — is MOV ESP, EBP and POP EBP instructions pair equivalent — in other words, this
instruction setting back stack pointer (ESP) and EBP register to its initial state.
This is necessary because we modified these register values (ESP and EBP) at the function start (executing MOV
EBP, ESP / AND ESP, ...).


```
