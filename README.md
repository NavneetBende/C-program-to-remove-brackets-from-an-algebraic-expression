Removing brackets from an algebraic expression.
In this article we will learn how to code a C program to remove brackets from an algebraic expression. We will be using a while loop that will iterate each character till the end of the string , and store the string in new character array . If brackets are found then we will skip them and as the iteration ends we will get an algebraic expression without brackets. 

C program to remove brackets from an algebraic expression
Algorithm:
Initialize the variables.
Accept the input.
Initialize a while loop and terminate it at the end of string. 
Iterate each character of the string through that loop.
Store these characters into an new array skip brackets , if found.
 Print result.
 
While loop in C
C programming code to remove brackets from an algebraic expression
#include<stdio.h>  
int main()
{
    //Initializing variables.
    char str[100] = "Prep))insta", str_no_spc[100];
    int i=0, j=0 ;
    
    //Iterating each character of string.
    while(str[i] != '\0')
    {
        if(str[i] != '(' &&  str[i] != ')')//Excluding brackets.
        {
            str_no_spc[j++] = str[i];
        }
        i++;
    }
    str_no_spc[j] = '\0';
    
    //Printing result.
    printf("The string after removing all the spaces is:\n%s", str_no_spc);
    return 0;
}
Output
The string after removing all the spaces is:
Prepinsta
Method 2
Here we are using the same concept as above but this is implemented using for loop.

#include<stdio.h>   
int main() {
     //Initializing variables.
    char str[100] = "P(r(e)p)Ins)ta", str_no_spc[100];
    int i = 0, j = 0 ;
       
    //Iterating each character of string.
    for (int i = 0; str[i] != '\0'; i++)
    {
       if (str[i] != '(' &&  str[i] != ')')  // Excluding brackets.
        {
              str_no_spc[j++] = str[i];
        }
    }

    str_no_spc[j] = '\0';
    //Printing result.
    printf("The string after removing all the spaces is:%s", str_no_spc);
       return 0;
}
Output
The string after removing all the spaces is:
PrepInsta
