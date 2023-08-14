Assignment 1

Print "Hello, World!" to the terminal

-----

#include <stdio.h>
```
main()
{
	printf("Hello World");
	return 0;
	
}
```
The code is represent like this:
```
; int __cdecl main(int argc, const char **argv, const char **envp)
main proc near
sub     rsp, 28h                        
lea     rcx, _Format    ; "Hello World"
call    printf
xor     eax, eax
add     rsp, 28h
retn
main endp
```
I have similar results with ghidra, but one thing interest is this 
```
       140001074  48  8d  0d       LEA        _Argc ,[s_Hello_World ]                          = "Hello World"
```
Ghidra move hello world to argc

In this case we see LEA, but sometimes see this instruction with mov. We can see push instruction too. We only put values on the stack.

With IDA&GH, rename our string with the name  "_Format". Compiler need to work with this string (hasn´t its own name)


WE see here:


```


RCX = Puede utilizarse para almacenar temporalmente datos, direcciones de memoria o valores de contador en ciertas instrucciones de contro

RSP = l registro "RSP" apunta a la cima de la pila en memoria, lo que significa que indica la dirección de memoria donde se almacenará el siguiente valor que se inserte en la pila.

LEA =  cargar la dirección de la cadena "_Format" en el registro RCX.
xor = eXclusive OR
	- The meaning of "xor   eax, eax" is return 0
	- He have diferent options, like MOV EAX, 0 (more opcodes)

RET = Last instruction RET returning control flow to calling function

```
