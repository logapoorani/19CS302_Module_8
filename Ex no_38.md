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
# EX 38 C Print a pattern of numbers from  to  as shown below. Each of the numbers is separated by a single space.
# DATE:
# AIM:
To Print a pattern of numbers from  to  as shown below. Each of the numbers is separated by a single space.
# Algorithm
1.Start.
2.Read the value of n.
3.Calculate size = 2 × n − 1.
4.Repeat for each row i from 0 to size − 1:
5.Repeat for each column j from 0 to size − 1:
6.Find the minimum distance of the current position from all four borders:
Top: i
Left: j
Bottom: size − i − 1
Right: size − j − 1
7.Store the smallest distance in min.
8.Print n − min.
9.Move to the next line after completing a row.
10.Stop.
# Program:
```
#include <stdio.h>
int main() {
    int n;
    scanf("%d", &n);
    int size = 2 * n - 1;
    for (int i = 0; i < size; i++) {
        for (int j = 0; j < size; j++) {
            int min = i < j ? i : j; 
            min = min < size - i ? min : size - i - 1;
            min = min < size - j - 1 ? min : size - j - 1;
            printf("%d ", n - min);
            }
            printf("\n");
        }
        return 0;
    }
```
# Output:
<img width="802" height="705" alt="Screenshot 2026-06-08 154056" src="https://github.com/user-attachments/assets/43a85284-0a7e-4372-840c-8f4f1d6cc989" />


# Result:
Thus the program was executed and the output was verified successfully.
