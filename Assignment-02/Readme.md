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

IDA:

```
var_28= qword ptr -28h
var_20= dword ptr -20h
var_1C= byte ptr -1Ch
var_18= qword ptr -18h

sub     rsp, 48h
mov     rax, cs:__security_cookie
xor     rax, rsp
mov     [rsp+48h+var_18], rax
mov     eax, cs:dword_140002258
lea     rcx, _Format    ; "%d is an integer!\n"
movsd   xmm0, qword ptr cs:aHelloW ; "Hello, W"
mov     edx, 5
mov     [rsp+48h+var_20], eax
movzx   eax, cs:byte_14000225C
mov     [rsp+48h+var_1C], al
movsd   [rsp+48h+var_28], xmm0
call    printf
movsd   xmm1, cs:__real@40091eb860000000
lea     rcx, aFIsAFloat ; "%f is a float!\n"
movq    rdx, xmm1
call    printf
lea     rdx, [rsp+48h+var_28]
lea     rcx, aSIsAnString ; "%s is an string!\n"
call    printf
xor     eax, eax
mov     rcx, [rsp+48h+var_18]
xor     rcx, rsp        ; StackCookie
call    __security_check_cookie
add     rsp, 48h
retn
main endp


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
