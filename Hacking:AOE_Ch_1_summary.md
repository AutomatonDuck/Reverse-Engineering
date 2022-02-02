#Programming

##Definition:

programming is creating a set of instructions to follow, that's it; Its that simple.

__Pseudo-Code__ is writing a program in plain english in a similar syntax to an actual programming language, its kind of the equivalent of measuring twice cutting once philosophy. 

```c++
main function{
    print("This is an example of pseudo-code");
    can_run_in_compiler = FALSE;
}
```

its a good way to get the logic and idea of a code block written down in way that it can be played with or give an aha moment.

Loops are standard programming control structures. They must consist of a check statement, and an exit condition lest the loop consists forever. If-then-else and while loops are the most common, <s>If i remember correctly switch statements and another kind exists I can remember</s> Conditional statements are control structures.

```C++
main function{
    while(this_condition_is = TRUE or 1{
        perform these instruction;
        this_condition_is = FALSE; // this whill break the while loop
        }
    if(number_of_iterations = 0; number_of_iterations < 10; increment number_of_iterations){
            perform these instructions;
            //number of iterations will increment by one every time all the code in the if statement is completed
            //This will provide the exit condition for the loop
    }
    else{
        perform these instructions
        //else will only execute when the above if statement is false and will only execute once
    }
}
```

Loops and conditional statements allow a block of code to be run multiple times, not be run at all, or be run under certain conditions. I feel like this is a gross simplification honestly.
In most languages the then in if-then-else statements is implied. Pascal uses them apparently.

All languages use variables which are really just assignments in memory for use by the program and programmer. There exist multiple types:
1.  Integer - int
2.  decimals - float or double
3.  letters - char

more exist but this is fine for now. And these variables can have multiple operations performed on them such as math operations, although math operations on char will give an error.
1. "+" - addition
2. "-" - subtraction
3. "*" - multiplication
4. "/" - division
5.  "%" - modulus

modulus returns the remainder of division. There are also comparison operators such as less then, greater or equal to, etc.
1. "<" - less than
2. ">" - greater than
3. "<=" - less than or equal to
4. ">=" - greater than or equal to
5. "==" - is equal to
6. "!=" - is not equal to

These can all be used in conditional statements, and variables can be compared to one another or compared to literals. (Literals are just pure values like 1 or a or 2.33) Of course logic is also present in programming so AND, OR logic can be used. XOR also exists within programming but it is a bitwise logic and that explanation will com later. 
* && - AND
* || - OR
* ! - NOT

Logic works like how it sounds. In an AND statement if all conditions are true, the statement is true, if any are false the whole statement is false. In an OR statement the statement is true is any condition is true, and false only when all conditions are false

###AND Truth Table
| A | B | Output |
|---|---|---|
| 0 | 0 | 0 |
| 1 | 0 | 0 |
| 0 | 1 | 0 |
| 1 | 1 | 1 |

###OR Truth Table
| A | B | Output |
|---|---|---|
| 0 | 0 | 0 |
| 1 | 0 | 0 |
| 0 | 1 | 0 |
| 1 | 1 | 1 |

Not just inverts, so !(TRUE) = FALSE. There also exists a world of boolean algebra where this logic is defined and manipulated and if your curious you can explore it along with De Morgan and his law.

Functions are code blocks that are created because they are used multiple times through a program, and instead if repeatedly writing the same line of code over and over you can create a function that you can call.
```C++
#include <stdio.h>
//function prototype
int add_two_numbers(int,int);
int main(void){
    int a = 7;
    int b = 8;
    int sum;
    sum = add_two_numbers(a,b);
    printf("&d", sum);
    return 0;
}
int add_two_numbers(int a, int b){
    sum = a + b;
    return sum;
}
```
The above is an actual executable C program which demonstrates a simple use of a function. Although it is only called once in the main function it can be called as many times as a programmer wants, you just have to type the name of the functions and ensure the proper variables are entered in the parentheses as seen above.
Another thing to point out is the `#include <stdio.h>`, this is a header file. C and C++ popularity is due to these header files. These header files are also known as libraries,which hold developed code and functions that can be used to simplify programming. The `printf()` function is defined in `stdio.h` which is also known as the standard input/output library.
Another thing I want to point out is the way the function `int add_two_numbers()` is presented in the program. First it is prefaced with `int`. The preface of a function is the type of variable that the function will return to whatever part of the program is calling it. In the example it returns an integer. In the main function where we call the `add_two_numbers()` function, sum is being initialized to the value the function is returning. I also wrote the function above the main function with the comment: function prototype. This simply a programming convention and used to keep things clean. The function could have been created there however it is the standard to have all functions created after the main function, that way debugging and code analysis can be done easier. However since programs run sequentially, the main function has to know the other functions exists, hence the function prototype being before the main function. 

One last note. the `return 0;` statement in main is just a way of saying the program executed without errors. As long as the program returns a value of 0 we know that no errors occurred(most times, error checking will be discussed else where).