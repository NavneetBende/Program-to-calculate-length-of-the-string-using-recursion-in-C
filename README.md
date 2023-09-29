# Program-to-calculate-length-of-the-string-using-recursion-in-C

Length of the String Using Recursion in C
Here, in this page we will discuss the program to find the length of the string using recursion in C Programming language. We are given with string and need to create a recursive function that will return the length of the string passed to it.

Length of the string using recusrion
Example
Input : String str :"Let's Learn C Programming"
Output :25

Input : String str :"PrepInsta"
Output :9
Algorithm :
In this method we will discuss the recursive way to find the length of the given input string

Create a recursive function.
Inside the main function call the recursive function by passing string and 0,
Now, the base condition of the recursive function is if(str[i]==’\0′) return 0,
Otherwise, we have to return 1+find_len(str, i+1).
Length of String Using Recursion in C
Code in C
Run
#include<stdio.h> 

int find_len (char [], int);

int main ()
{
	char str[100]="Let's Learn C Programming";
	int len = 0;
    
	len = find_len (str, 0);
    
    printf ("The length of the given string is: %d\n", len);
	return 0;

}

int find_len (char str[], int index){

	static int l = 0;

	if (str[index] == '\0')
		return l;

	else
		l ++;
	find_len (str, index + 1);
}
Output :
