#Assembly & Disassembly

**Note:The following code and information will all be Linux based.**
##C and ASM
C is a complied language, which means that the C program is translated to machine instructions
which is then executed by the computer. C was developed to allow for cross platform programming between
the various types of CPU architectures, such as the x86, sparc, etc. Each of these architectures has 
a different set of machine code, and can because of this trying to develop programs in the native machine language of
each architecture is unreasonable. A complied language can be translated to whatever architecture is needed so
only one version of the program needs to be written(in theory) A complier(such as GCC) complies the language. There are many more steps in the processes but lets keep it simple for now. C is considered a high-level language
```C
#include <stdio.h>

int main(){
    int i;
    for(i = 0;i<10;i++){
        printf("Hello World");
    }
    return 0;
}
```
This is an example of a C program

ASM also called assembly is a low level language and represents actual machine language instructions. Within ASM you can see addresses, registers, bytes, and operations that a processor is performing. This is important for reverse-engineering as here in assembly we can put a program under a microscope and evaluate every little thing it is doing, and with the right tools, find out why its doing it.

![Disassembled C program](images/hello_world_loop_asn.png)
