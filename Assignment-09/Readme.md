Assignment 9

Take two command line arguments from the user, their first and last name, and then print a welcome message for the user.

The program should check for two arguments and then print the program's usage instructions if the user submits too few or too many arguments.

Example
```
tokyo:~/LearningC/ # ./assignment9                                   
Usage: ./assignment9 Firstname Lastname#
tokyo:~/LearningC/ # ./assignment9 Jimmy Smith                      
Hello, Jimmy Smith#
tokyo:~/LearningC/ # ./assignment9 Jimmy Paul Smith                  
Usage: ./assignment9 Firstname Lastname#
```
--------

Code 
```
#include <stdio.h>

// defining main with arguments
int main(int argc, char* argv[])
{
    printf("You have entered %d arguments, only accept 3\n", argc);

    if (argc < 3) {
        printf("Usage: ./assignment9 Firstname Lastname#");
    }

    else if (argc > 3) {
        printf("Usage: ./assignment9 Firstname Lastname#");
    }

    char *nombre = argv[1];
    char *apellido = argv[2];

    printf("Hello, %s %s\n", nombre, apellido);

    return 0;
}
```
### Random
Nunca me había planteado que un programa, como podría ser ls, la forma de aceptar argumentos se a esta..... y la de veces que lo he usado! Buenisimo.


IDA
jz =     The jz instruction is a conditional jump that follows a test.
    It jumps to the specified location if the Zero Flag (ZF) is set (1).
    jz is commonly used to explicitly test for something being equal to zero whereas je is commonly found after a cmp instruction.

