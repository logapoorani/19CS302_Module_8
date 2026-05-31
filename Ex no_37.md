
# # Hackerrank problem - 2

Your task is to take two numbers of int data type, two numbers of float data type as input and output their sum:

Declare 4 variables: two of type int and two of type float.

Read 2 lines of input from stdin (according to the sequence given in the 'Input Format' section below) and initialize your variables.

Use the + and - operator to perform the following operations:

Print the sum and difference of two int variable on a new line.

Print the sum and difference of two float variable rounded to one decimal place on a new line.

## Input Format

The first line contains two integers.

The second line contains two floating point numbers.

## Constraints 

1 ≤ integer variables ≤ 104

1 ≤ float variables ≤ 104

## Output Format

Print the sum and difference of both integers separated by a space on the first line, and the sum and difference of both float (scaled to 1 decimal place) separated by a space on the second line.

Sample Input 

10 4

4.0 2.0

Sample Output 

14 6

6.0 2.0

Explanation

When we sum the integers 10 and 4, we get the integer 14. When we subtract the second number 4 from the first number 10, we get 6 as their difference.

When we sum the floating-point numbers 4.0 and 2.0, we get 6.0. When we subtract the second number 2.0 from the first number 4.0, we get 2.0 as their difference.



# EX 31 C program to find the smallest among three numbers using Structure.
## DATE:
## AIM:
To write a C program to find the smallest among three numbers using Structure.

## Algorithm
1.Start the program and define a structure with three integer fields.

2.Declare a structure variable to store the three numbers.

3.Read the values of the three numbers from the user.

4.Compare the three numbers to find the smallest.

5.Display the smallest number and end the program. 

## Program:
```
/*
C program to find the smallest among three numbers using Structure.
*/
#include <stdio.h>

struct Numbers
{
    int num1, num2, num3;
};

int main()
{
    struct Numbers n;

    printf("Enter three numbers: ");
    scanf("%d %d %d", &n.num1, &n.num2, &n.num3);

    int smallest = n.num1;

    if(n.num2 < smallest)
    {
        smallest = n.num2;
    }

    if(n.num3 < smallest)
    {
        smallest = n.num3;
    }

    printf("The smallest number is: %d\n", smallest);

    return 0;
}


```

## Output:

![image](https://github.com/user-attachments/assets/d887c1cc-83cb-4eee-aa33-50eed14d157c)


## Result:
Thus the program was executed and the output was verified successfully.
