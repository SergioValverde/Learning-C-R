
Intialize and delcare an int variable with any value. Assign a pointer variable to the int variable you just declared and then print the value of the pointer variable.


```
tokyo:~/LearningC/ # ./assignment14                                       
The value of our pointer is: -1081381992
```

-----
###CODe

```
#include <stdio.h>

int main() {
   
    int p = 1;

    int *pp = &p;

    printf("The value of our pointer is: %p", pp);

    return 0;
}
```
