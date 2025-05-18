EXP NO:21 C PROGRAM TO CREATE A FUNCTION TO FIND THE GREATEST NUMBER 

Aim: To write a C program to create a function to find the greatest number

Algorithm:
```
Include the necessary header #include <stdio.h>.
Use a series of if and else if statements to compare the values and return the maximum among them.
Declare variables n1, n2, n3, n4, and greater to store user input and the result.
Use scanf to take four integers as input.
Call the max_of_four function with the input integers and store the result in the greater variable
```
Program: 
```
#include<stdio.h>
int max(int a, int b, int c, int d);
int main()
{
    int a,b,c,d;
    scanf("%d %d %d %d",&a, &b, &c, &d);
    int x = max(a,b,c,d);
    printf("%d",x);
}
int max(int a, int b, int c, int d)
{
    if(a>b && a>c && a>d)
    {
        return a;
    }
    else if (b>c && b>d)
    {
        return b;
    }
    else if(c>d)
    {
        return c;
    }
    else
    {
        return d;
    }
}
```
Output:
![image](https://github.com/user-attachments/assets/25872754-0050-4588-b207-3f72131437fd)


Result: Thus, the program that create a function to find the greatest number is verified successfully.

EXP NO:22 C PROGRAM TO PRINT THE MAXIMUM VALUES FOR THE AND, OR AND XOR COMPARISONS 

Aim: To write a C program to print the maximum values for the AND, OR and XOR comparisons

Algorithm:
```
Define a function calculate_the_max that takes two integers n and k as parameters.
Declare variables a, o, and x to store the maximum values for AND, OR, and XOR operations, respectively.
Use nested loops to iterate through pairs of integers (i, j) from 1 to n.
Within the loops, check conditions for AND, OR, and XOR operations and update the corresponding maximum values (a, o, x).
Declare variables n and k to store user input.
Use scanf to take two integers as input.
Call the calculate_the_max function with input values.
```
Program: 
```
#include <stdio.h>
void maximum(int n, int k);
int main() 
{
    int n, k;
    scanf("%d %d", &n, &k);
    maximum(n, k);
}

void maximum(int n, int k)
{
    int maxand = 0;
    int maxor = 0;
    int maxxor = 0;
    for (int i = 1; i < n; i++) 
    {
        for (int j = i+1; j <= n; j++)
        {
            int andval = i & j;
            int orval = i | j;
            int xorval = i ^ j;

            if (andval < k && andval > maxand) 
            {
                maxand = andval;
            }
            if (orval < k && orval > maxor)
            {
                maxor = orval;
            }
            if (xorval < k && xorval > maxxor)
            {
                maxxor = xorval;
            }
        }
    }
    printf("%d\n%d\n%d\n", maxand,maxor,maxxor);
}
```
Output: 
![image](https://github.com/user-attachments/assets/adf3fcad-ec61-4b35-9af7-bc33d54a12d6)


Result: Thus, the program to print the maximum values for the AND, OR and XOR comparisons is verified successfully.

EXP NO:23 C PROGRAM TO WRITE THE LOGIC FOR THE REQUESTS 

Aim: To write a C program to write the logic for the requests

Algorithm:
```
Declare variables noshel and noque to store the number of shelves and the number of queries, respectively.
Use scanf to take two integers as input for the number of shelves and queries.
Declare a 2D array shelarr to represent shelves and books, and an array nobookarr to store the number of books on each shelf.
Declare variables k and c to keep track of the book index and the total number of books.
Use a for loop to iterate over the queries.
```
Program: 
```
#include<stdio.h>
int main()
{
    int s;
    int n;
    scanf("%d %d",&s,&n);
    int lib[1000][1000]={0};
    int cnt[1000]={0};
    for(int i=0;i<n;i++)
    {
        int qt,x,y;
        scanf("%d",&qt);
        if(qt==1)
        {
            scanf("%d %d",&x,&y);
            lib[x][cnt[x]]=y;
            cnt[x]++;
        }
        if(qt==2)
        {
            scanf("%d %d",&x,&y);
            printf("%d",lib[x][y]);
        }
        if(qt==3)
        {
            scanf("%d",&x);
            printf("%d",cnt[x]);
        }
    }
}
```
Output:
![image](https://github.com/user-attachments/assets/af9a23ec-6781-4b82-8e2a-b8c7f3f41a9f)

Result: Thus, the program to write the logic for the requests is verified successfully.

EXP NO:24 C PROGRAM PRINT THE SUM OF THE INTEGERS IN THE ARRAY.

Aim: To write a C program print the sum of the integers in the array.

Algorithm:
```
Declare a variable n to store the number of integers.
Use scanf to take an integer n as input.
Declare an array a of size n to store the integers.
Declare a variable sum and initialize it to zero.
Use a for loop to iterate n times:
Use scanf to input each integer and add it to the sum.
Print the final sum using printf.
```
Program: 
```
#include<stdio.h>
#include<stdlib.h>
int main()
{
    int n;
    int s=0;
    scanf ("%d",&n);
    int *ptr;
    ptr=(int*)malloc(n*sizeof (int));
    for (int i=0;i<n;i++)
    {
        scanf ("%d",ptr+i);
    }
     for (int i=0;i<n;i++)
     {
         s+=ptr[i];
     }
     printf ("%d",s);
}
```

Output: 
![image](https://github.com/user-attachments/assets/0dd35af0-e022-456a-8685-4dcb21f30084)


Result: Thus, the program prints the sum of the integers in the array is verified successfully.

EXP NO 25: C PROGRAM TO COUNT THE NUMBER OF WORDS IN A SENTENCE

Aim:

To write a C program that counts the number of words in a given sentence.

Algorithm:
```
Input the sentence: Take a sentence from the user.
Initialize a counter variable: This will keep track of the number of words.
Process each character of the sentence: o Iterate through the sentence, checking each character. o If a character is not a space, it may belong to a word. If it's the first non-space character after a space or at the start, increment the word count.
Handle spaces and punctuation: Skip over spaces, punctuation marks, and consider each word as a sequence of characters separated by spaces.
Display the result: After processing the sentence, output the total word count.
```
Program: 
```
#include<stdio.h>
#include<string.h>
#include<ctype.h>
int main()
{
    char a[100];
    scanf("%[^\n]",a);
    int c=1;
    for(int i=0; a[i]!='\0'; i++)
    {
        if(a[i]==32)
        {
            c++;
        }
    }
    printf("%d",c);
}
```

Output: 
![image](https://github.com/user-attachments/assets/428ef9b0-c4d2-4d70-9f33-1bcfc418c4fb)

Result:

Thus, the program that counts the number of words in a given sentence is verified successfully.
