## Given an array of strings sorted in lexicographical order, print all of its permutations in strict lexicographical order. If two permutations look the same, only print one of them. See the 'note' below for an example.

Complete the function next_permutation which generates the permutations in the described order.

## For example, s=[ab,bc,cd]. The six permutations in correct order are:

ab bc cd
ab cd bc
bc ab cd
bc cd ab
cd ab bc
cd bc ab
Note: There may be two or more of the same string as elements of .
## For example, s=[ab,bc,cd]. Only one instance of a permutation where all elements match should be printed. In other words, if s[0]==s[1], then print either s[0]  or s[1] but not both.

A three element array having three distinct elements has six permutations as shown above. In this case, there are three matching pairs of permutations where ab and ba are switched. We only print the three visibly unique permutations:

ab ab bc
ab bc ab
bc ab ab
## Input Format

The first line of each test file contains a single integer , the length of the string array .

Each of the next  lines contains a string .

Constraints

 contains only lowercase English letters.
Output Format

Print each permutation as a list of space-separated strings on a single line.

## Sample Input 0

2
ab
cd
## Sample Output 0

ab cd
cd ab
## Sample Input 1

3
a
bc
bc
## Sample Output 1

a bc bc
bc a bc
bc bc a



# EX 40 C program to print each permutation as a list of space-separated strings on a single line.
## DATE:23/04/2026
## AIM:
To write a C program to print each permutation as a list of space-separated strings on a single line.

## Algorithm
1.Start the program by reading the integer n and the array of strings from the user.

2.Sort the array of strings to ensure lexicographical order.

3.Generate the next permutation using the next_permutation() function.

4.Print each permutation without duplicates by keeping track of previously printed permutations.

5.End the program.

## Program:
```
/*
C program to find the smallest among three numbers using Structure.
*/
#include <stdio.h>
#include <string.h>
#include <stdlib.h>

void swap(char *x, char *y)
{
    char temp[100];
    strcpy(temp, x);
    strcpy(x, y);
    strcpy(y, temp);
}

int compare(const void *a, const void *b)
{
    return strcmp(*(const char **)a, *(const char **)b);
}

int next_permutation(char *arr[], int n)
{
    int i = n - 2;
    while(i >= 0 && strcmp(arr[i], arr[i + 1]) >= 0)
        i--;
    if(i < 0)
        return 0;
    
    int j = n - 1;
    while(strcmp(arr[i], arr[j]) >= 0)
        j--;
    
    swap(arr[i], arr[j]);
    int k = i + 1;
    j = n - 1;
    while(k < j)
    {
        swap(arr[k], arr[j]);
        k++;
        j--;
    }
    
    return 1;
}

int main()
{
    int n;
    scanf("%d", &n);

    char *arr[n];
    for(int i = 0; i < n; i++)
    {
        arr[i] = (char *)malloc(100 * sizeof(char));
        scanf("%s", arr[i]);
    }

    qsort(arr, n, sizeof(char *), compare);

    do
    {
        for(int i = 0; i < n; i++)
            printf("%s ", arr[i]);
        printf("\n");
    } while(next_permutation(arr, n));

    return 0;
}



```

## Output:

![image](https://github.com/user-attachments/assets/b3f22347-b4fc-4491-9710-da42da5101aa)


## Result:
Thus the program was executed and the output was verified successfully.
