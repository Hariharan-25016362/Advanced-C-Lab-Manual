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
 
### Program:
```
#include <stdio.h>
int main() {
    int n;
    printf("Enter a number: ");
    scanf("%d", &n);
switch (n) {
    case 1:
       printf("one\n");
       break;
    case 2:
       printf("two\n");
       break;
    case 3:
       printf("three\n");
       break;
    case 4:
       printf("four\n");
       break;
    case 5:
       printf("five\n");
       break;
    case 6:
       printf("six\n");
       break;
    case 7:
       printf("seven\n");
       break;
    case 8:
       printf("eight\n");
       break;
    case 9:
       printf("nine\n");
       break;
    case 10:
       printf("ten\n");
       break;
    case 11:
       printf("eleven\n");
       break;
    case 12:
       printf("twelve\n");
       break;
    case 13:
       printf("thirteen\n");
       break;
    default:
       printf("Greater than 13\n");
       break;
}
return 0;
}
```








### Output:

<img width="450" height="253" alt="image" src="https://github.com/user-attachments/assets/11a01186-30c0-49ea-a5c1-a1980daea0b4" />










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
 
### Program:
```
#include <stdio.h>
int main() {
    char a[50];
    int i, h, c;
    printf("Enter a string of digits: ");
    scanf("%s", a);
    for (h = 0; h <= 3; h++) {
        c = 0;
        for (i = 0; a[i] != '\0'; i++) {
            if (a[i] - '0' == h) {
                c++;
            }
        }
        printf("%d ", c);
    }

    printf("\n");
    return 0;
}
```






### Output:
<img width="566" height="232" alt="image" src="https://github.com/user-attachments/assets/94792926-e5a2-472b-a431-29f7c1b63422" />










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
 
### Program:
```
#include <stdio.h>
#include <stdlib.h>
#include <string.h>
int next_permutation(int n, char **s)
{
     int k, l;
  for (k = n - 2; k >= 0; k --)
 {
    if(strcmp(s[k], s[k+1]) < 0) break;
  }
  if (k < 0) return 0;
  for (l = n -1; l > k; l --)
 {
    if(strcmp(s[k], s[l]) < 0) break;
  }
  char * tmp = s[k];
  s[k] = s[l];
  s[l] = tmp;
  for(int i = k + 1, j = n -1; i < j; i ++, j --)
 {
    tmp = s[i];
    s[i] = s[j];
    s[j] = tmp;
  }
  return 1;
}
int main()
{
    char **s;
    int n;
    scanf("%d", &n);
    s = calloc(n, sizeof(char*));
    for (int i = 0; i < n; i++)
    {
        s[i] = calloc(11, sizeof(char));
        scanf("%s", s[i]);
    }
    do
    {
        for (int i = 0; i < n; i++)
            printf("%s%c", s[i], i == n - 1 ? '\n' : ' ');
    } while (next_permutation(n, s));
    for (int i = 0; i < n; i++)
        free(s[i]);
    free(s);
    return 0;
}

```






### Output:
<img width="476" height="304" alt="image" src="https://github.com/user-attachments/assets/b20688eb-3c5c-4c8b-8f50-00f59c3047a3" />









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
 
### Program:

```
#include <stdio.h>
int main() {
    int n, i, j, len, min;
    printf("Enter the value of n: ");
    scanf("%d", &n);
    len = n * 2 - 1;
    for (i = 0; i < len; i++) {
        for (j = 0; j < len; j++) {
            min = (i < j) ? i : j;
            min = (min < len - i - 1) ? min : len - i - 1;
            min = (min < len - j - 1) ? min : len - j - 1;
            printf("%d ", n - min);
    }
    printf("\n");
 }
 return 0;
}
```



### Output:

<img width="610" height="439" alt="image" src="https://github.com/user-attachments/assets/2a6e5350-f075-41ad-880b-8167a7273108" />







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

### Program:

```
#include <stdio.h>
int square() {
    int num;
    printf("Enter a number: ");
    scanf("%d", &num);
    return num * num;
}
int main() {
   int result = square();
   printf("The square of the number is: %d\n", result);
   return 0;
}
```




### Output:


<img width="498" height="211" alt="image" src="https://github.com/user-attachments/assets/b1395cc2-e9e3-4cb4-8e41-d17b91320ebb" />






Result:
Thus, the program is verified successfully



























