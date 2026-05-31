
# # Task

# # Given a positive integer denoting , do the following:

# If  41<=n <=49 print the lowercase English word corresponding to the number (e.g., forty one for 41 , forty two for 42 etc.).
If n>49 print Greater than 49.
## Input Format

The first line contains a single integer, .

## Constraints

## Output Format

If  41<=n <=49 print the lowercase English word corresponding to the number (e.g., forty one for 4 , forty two for 42 etc.).
If n>49 print Greater than 49.
## Sample Input

41
## Sample Output

forty one


# EX 38 C program to print the lowercase English word corresponding to the number.
## DATE:
## AIM:
To write a C program to print the lowercase English word corresponding to the number.

## Algorithm
1.Start the program and declare an integer variable to store input.

2.Read the integer input from the user.

3.Use a switch or if-else ladder to match numbers from 41 to 49 with their word form.

4.If the number is greater than 49, print "Greater than 49".

5.End the program.

## Program:
```
/*
C program to find the smallest among three numbers using Structure.
*/
#include <stdio.h>

int main()
{
    int n;
    scanf("%d", &n);

    if(n == 41)
        printf("forty one\n");
    else if(n == 42)
        printf("forty two\n");
    else if(n == 43)
        printf("forty three\n");
    else if(n == 44)
        printf("forty four\n");
    else if(n == 45)
        printf("forty five\n");
    else if(n == 46)
        printf("forty six\n");
    else if(n == 47)
        printf("forty seven\n");
    else if(n == 48)
        printf("forty eight\n");
    else if(n == 49)
        printf("forty nine\n");
    else if(n > 49)
        printf("Greater than 49\n");

    return 0;
}



```

## Output:

![image](https://github.com/user-attachments/assets/50294e17-cffe-4725-8624-52bc55a10912)


## Result:
Thus the program was executed and the output was verified successfully.
