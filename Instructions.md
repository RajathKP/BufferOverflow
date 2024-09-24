Buffer Overflow pt1
In this example you will compile and run a program in C. The program is already provided as bufoverflow.c 
- a simple program that creates a buffer and then asks you for a name, and prints it back out to the screen.
Enter the following code into a file called bufoverflow.c:

#include <stdio.h>

int main(int argc, char **argv)
{
    char buf[8];             // buffer for eight characters
    printf("Enter name: ");
    gets(buf);               // read from stdio (sensitive function!)
    printf("%s\n", buf);     // print out data stored in buf
    return 0;                // 0 as return value
}

Now use the rocket icon to compile and run the code.
To test it enter your first name (or at least the first 8 characters of it) you should get the output 
which is just your name repeated back to you.
Run the code a second time 
(from the command window this can be achieved by entering ./bufoverflow on the command line) 
this time enter a string of 10 or more characters. What happens? What does the output message mean? 
Be prepared to discuss you thoughts at this week’s seminar.