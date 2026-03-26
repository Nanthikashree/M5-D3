# M5-D3
AIM:
Write a C program to read matrix [3x3] that checks if the sum of major(main) and minor(off) diagonal elements are the same or not.


Input

Input elements of matrix:
1 2 1
4 5 6
9 8 9
Output
Major Diagonal Elements : 1 5 9

Minor Diagonal Elements : 1 5 9

Sum of Major Diagonal Elements : 15

Sum of Minor Diagonal Elements : 15

Sum is SAME
PROGRAM:
```
#include <stdio.h>

int main()
{
    int a[3][3];
    int i, j;
    int majorSum = 0, minorSum = 0;

   
    for(i = 0; i < 3; i++)
    {
        for(j = 0; j < 3; j++)
        {
            scanf("%d", &a[i][j]);
        }
    }
    for(i=0;i<3;i++)
    {
        for(j=0;j<3;j++)
        {
            printf("%d ",a[i][j]);
        }
        printf("\n");
    }
    printf("\n");

    // Major diagonal
    printf("Major Diagonal Elements : ");
    for(i = 0; i < 3; i++)
    {
        printf("%d ", a[i][i]);
        majorSum += a[i][i];
    }

    // Minor diagonal
    printf("\n\nMinor Diagonal Elements : ");
    for(i = 0; i < 3; i++)
    {
        printf("%d ", a[i][2 - i]);
        minorSum += a[i][2 - i];
    }

    // Print sums
    printf("\n\nSum of Major Diagonal Elements : %d", majorSum);
    printf("\n\nSum of Minor Diagonal Elements : %d", minorSum);

    // Check condition
    if(majorSum == minorSum)
        printf("\n\n Sum is SAME");
    else
        printf("\n\n Sum is NOT SAME");

    return 0;
}
```
OUTPUT:
<img width="992" height="878" alt="image" src="https://github.com/user-attachments/assets/8a65c3af-ee34-4881-a367-aa637d71a39d" />
RESULT:
Thus the code run successfully!

