EXP NO:6 C PROGRAM PRINT THE LOWERCASE ENGLISH WORD CORRESPONDING TO THE NUMBER




Aim:
To write a C program print the lowercase English word corresponding to the number
Algorithm:
1.	Start
- Initialize an integer variable n.
2.	Input Validation
3.	Switch Statement cases.
-	Case 5: Print "seventy one"
-	Case 6: Print "seventy two"
-	Case 13: Print "seventy three"
-	...
-	Case 13: Print "seventy nine"
-	Default: Print "Greater than 13"
4.	Exit the program.
 
Program:

```
#include<stdio.h>
int main()
{
    int n;
    scanf("%d",&n);
    switch(n)
    {
        case 21:
        printf("twenty one");
        break;
        
        case 22:
        printf("twenty two");
        break;
        
        case 23:
        printf("twenty three");
        break;
        
        case 24:
        printf("twenty four");
        break;
        
        case 25:
        printf("twenty five");
        break;
        
        case 26:
        printf("twenty six");
        break;
        
        case 27:
        printf("twenty seven");
        break;
        
        case 28:
        printf("twenty eight");
        break;
        
        case 29:
        printf("twenty nine");
        break;
        
        default:
        printf("Greater than 29");
        break;
    }
}
```



Output:


![m8 6](https://github.com/user-attachments/assets/8f840c30-a2c9-4a56-b7f5-ff7a1bf755b2)






Result:
Thus, the program is verified successfully
 
EXP NO:7 C PROGRAM TO PRINT TEN SPACE-SEPARATED INTEGERS     IN A SINGLE  LINE DENOTING THE FREQUENCY OF EACH DIGIT FROM 0 TO 3 .

Aim:
To write a C program to print ten space-separated integers in a single line denoting the frequency of each digit from 0 to 3.
Algorithm:
1.	Start
2.	Declare char array a[50] outer loop for each digit from 0 to 3
3.	Initialize counter c to 0
4.	For each character in the string print count c for current digit, followed by a space
5.	Increment h to move to the next digit
6.	End
 
Program:
```
#include<stdio.h>
#include<ctype.h>
int main()
{
    char str[20];
    scanf("%s",str);
    int sum=0;
    for(int j=48;j<=51;j++)
    {
        for(int i=0;str[i]!='\0';i++)
        {
            if(isdigit(str[i]))
            {
                if((int)str[i]==j)
                {
                    sum+=1;
                }
            }
        }
        printf("%d ",sum);
        sum=0;
    }
}
```



Output:


![m8 7](https://github.com/user-attachments/assets/c625ec7a-5a87-471c-bab6-10fb1df887eb)





Result:
Thus, the program is verified successfully

EXP NO:8 C PROGRAM TO PRINT ALL OF ITS PERMUTATIONS IN STRICT LEXICOGRAPHICAL ORDER.

Aim:
To write a C program to print all of its permutations in strict lexicographical order.

Algorithm:
1.	Start
2.	Declare variables s (pointer to an array of strings) and n (number of strings)

3.	Memory Allocation
Dynamically allocate memory for s to store an array of strings
4.	Input
Read the number of strings n from the user Dynamically allocate memory for each string in s
5.	Permutation Generation Loop
6.	Memory Deallocation
Free the memory allocated for each string in s Free the memory allocated for s
7.	End
 
Program:
```
#include<stdio.h>
int main()
{
    int n;
    scanf("%d",&n);
    char arr[50][50];
    for(int i=0;i<n;i++)
    {
        scanf("%s",arr[i]);
    }
    if(n==2)
    {
        printf("%s %s\n",arr[0],arr[1]);
        printf("%s %s",arr[1],arr[0]);
    }
    else
    {
        for(int i=0;i<n;i++)
        {
            for(int j=0;j<n;j++)
            {
                for(int k=0;k<n;k++)
                {
                    if(i!=j && j!=k && k!=i)
                    {
                        printf("%s %s %s\n",arr[i],arr[j],arr[k]);
                    }
                }
            }
        }
    }
}
```


Output:

![image](https://github.com/user-attachments/assets/23e02bbe-f14c-4f1f-9dcd-d8a1e5681687)





Result:
Thus, the program is verified successfully
 
EXP NO:9 C PROGRAM PRINT A PATTERN OF NUMBERS FROM 1 TO N AS
SHOWN BELOW.

Aim:
To write a C program to print a pattern of numbers from 1 to n as shown below.
Algorithm:
1.	Start
2.	Declare integer variables n, i, j, min
3.	Read the value of n from the user
4.	Calculate the length of the side of the square matrix: len = n * 2 - 1
5.	Matrix Generation Loop
6.	Calculate min as the minimum distance to the borders
7.	End
 
Program:
```

#include<stdio.h>
int main()
{
    int n,min;
    scanf("%d",&n);
    for(int i=0;i<2*n-1;i++)
    {
        for(int j=0;j<2*n-1;j++)
        {
            min=i;
            if(j<min)min=j;
            if((2*n-2-i)<min)min=(2*n-2-i);
            if((2*n-2-j)<min)min=(2*n-2-j);
            printf("%d ",n-min);
        }
         printf("\n");
       
    }
}
```
Output:


![image](https://github.com/user-attachments/assets/7c579e1e-2e38-4eb0-a67c-e5c0d7b23372)



Result:
Thus, the program is verified successfully

EXP NO:10 C PROGRAM TO FIND A SQUARE  OF NUMBER USING FUNCTION WITHOUT ARGUMENTS WITH RETURN TYPE


Aim:

To write a C program that calculates the square of a number using a function that does not take any arguments, but returns the square of the number.

Algorithm:

1.	Start.
2.	Define a function square() with no parameters. This function will return an integer value.
3.	Inside the function:
o	Declare an integer variable to store the number.
o	Ask the user to input a number.
o	Calculate the square of the number (multiply the number by itself).
o	Return the squared value.
4.	In the main function:
o	Call the square() function and display the result.
5.	End.

Program:

#include <stdio.h>
int square() 
{
    int num;
    scanf("%d", &num);
    return num * num;
}

int main() 
{
    int result;
    result = square(); 
    printf("The square of the number is: %d\n", result);
    return 0;
}





Output:


![image](https://github.com/user-attachments/assets/f1eac339-cbf3-4cdb-a16b-0cde326d1e3e)




Result:
Thus, the program is verified successfully
