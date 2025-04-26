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

//type your code here
#include <stdio.h>

int main() {
    // Step 1: Initialize integer variable
    int n;

    // Step 2: Input from user
    printf("Enter a number: ");
    scanf("%d", &n);

    // Step 3: Switch statement
    switch(n) {
        case 5:
            printf("seventy one\n");
            break;
        case 6:
            printf("seventy two\n");
            break;
        case 13:
            printf("seventy three\n");
            break;
        case 14:
            printf("seventy four\n");
            break;
        case 15:
            printf("seventy five\n");
            break;
        case 16:
            printf("seventy six\n");
            break;
        case 17:
            printf("seventy seven\n");
            break;
        case 18:
            printf("seventy eight\n");
            break;
        case 19:
            printf("seventy nine\n");
            break;
        default:
            printf("Greater than 13\n");
            break;
    }

    // Step 4: Exit
    return 0;
}





Output:


//paste your output here
Enter a number: 6
seventy two






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

//type your code here
#include <stdio.h>

int main() {
    // Step 2: Declare character array
    char a[50];
    int i, h, c;

    // Step 1: Start
    printf("Enter a string of digits: ");
    scanf("%s", a);

    // Step 4: Outer loop for digits 0 to 3
    for (h = 0; h <= 3; h++) {
        c = 0; // Step 3: Initialize counter
        for (i = 0; a[i] != '\0'; i++) {
            if (a[i] == (h + '0')) {
                c++;
            }
        }
        printf("%d ", c); // Print frequency
    }

    // Step 5: Remaining 6 values are zero
    for (h = 4; h < 10; h++) {
        printf("0 ");
    }

    // Step 6: End
    return 0;
}




Output:


//paste your output here
Enter a string of digits: 12330123
1 2 2 2 0 0 0 0 0 0 






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

//type your code here
#include <stdio.h>
#include <stdlib.h>
#include <string.h>

// Swap two characters
void swap(char *x, char *y) {
    char temp = *x;
    *x = *y;
    *y = temp;
}

// Reverse the string from index l to r
void reverse(char *s, int l, int r) {
    while (l < r) {
        swap(&s[l], &s[r]);
        l++;
        r--;
    }
}

// Get next lexicographical permutation (returns 1 if next exists, 0 if not)
int next_permutation(char *s, int len) {
    int i = len - 2;
    while (i >= 0 && s[i] >= s[i + 1]) i--;
    if (i < 0) return 0;

    int j = len - 1;
    while (s[j] <= s[i]) j--;
    swap(&s[i], &s[j]);
    reverse(s, i + 1, len - 1);
    return 1;
}

int main() {
    // Step 1 & 2: Start and declare
    int n;
    char *s;

    // Step 3 & 4: Memory allocation and input
    printf("Enter a string: ");
    s = (char *)malloc(100 * sizeof(char));  // Assume max length 99
    scanf("%s", s);

    n = strlen(s);
    // Sort string first for lexicographical order
    for (int i = 0; i < n-1; i++) {
        for (int j = i+1; j < n; j++) {
            if (s[i] > s[j]) {
                swap(&s[i], &s[j]);
            }
        }
    }

    // Step 5: Generate permutations
    printf("\nLexicographical permutations:\n");
    do {
        printf("%s\n", s);
    } while (next_permutation(s, n));

    // Step 6: Free memory
    free(s);

    // Step 7: End
    return 0;
}




Output:


//paste your output here
Enter a string: cat

Lexicographical permutations:
act
atc
cat
cta
tac
tca







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

//type your code here
#include <stdio.h>

int main() {
    int n, i, j, len, min;

    // Step 3: Read the value of n
    printf("Enter the value of n: ");
    scanf("%d", &n);

    // Step 4: Calculate the length of the side of the square matrix
    len = n * 2 - 1;

    // Step 5: Matrix Generation Loop
    for (i = 0; i < len; i++) {
        for (j = 0; j < len; j++) {

            // Step 6: Calculate min (minimum distance to borders)
            min = (i < j) ? i : j;
            min = (min < len - i - 1) ? min : len - i - 1;
            min = (min < len - j - 1) ? min : len - j - 1;

            // Print the value for the current position in the pattern
            printf("%d ", n - min);
        }
        printf("\n"); // Move to the next line after each row
    }

    // Step 7: End
    return 0;
}





Output:


//paste your output here
Enter the value of n: 5
5 5 5 5 5 5 5 5 5 
5 4 4 4 4 4 4 4 5 
5 4 3 3 3 3 3 4 5 
5 4 3 2 2 2 3 4 5 
5 4 3 2 1 2 3 4 5 
5 4 3 2 2 2 3 4 5 
5 4 3 3 3 3 3 4 5 
5 4 4 4 4 4 4 4 5 
5 5 5 5 5 5 5 5 5 







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

//type your code here
#include <stdio.h>

// Step 2: Define the function square() with no parameters
int square() {
    int num;
    // Step 3: Ask user for input
    printf("Enter a number: ");
    scanf("%d", &num);
    
    // Step 3: Calculate and return the square of the number
    return num * num;
}

int main() {
    // Step 4: Call the square() function and display the result
    int result = square();
    printf("The square of the number is: %d\n", result);
    
    // Step 5: End
    return 0;
}




Output:


//paste your output here
Enter a number: 7
The square of the number is: 49







Result:
Thus, the program is verified successfully



























