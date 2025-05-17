

EXP NO:21 C PROGRAM TO CREATE A FUNCTION TO FIND THE GREATEST NUMBER
Aim:
To write a C program to create a function to find the greatest number

Algorithm:
1.	Include the necessary header #include <stdio.h>.
2.	Use a series of if and else if statements to compare the values and return the maximum among them.
3.	Declare variables n1, n2, n3, n4, and greater to store user input and the result.
4.	Use scanf to take four integers as input.
5.	Call the max_of_four function with the input integers and store the result in the greater variable
 
Program:
#include <stdio.h>

int max_of_four(int n1, int n2, int n3, int n4) {
    int max = n1;
    if (n2 > max) max = n2;
    if (n3 > max) max = n3;
    if (n4 > max) max = n4;
    return max;
}

int main() {
    int n1, n2, n3, n4;
    printf("Enter four integers: ");
    scanf("%d %d %d %d", &n1, &n2, &n3, &n4);

    int greater = max_of_four(n1, n2, n3, n4);
    printf("The greatest number is: %d\n", greater);

    return 0;
}


Output:
Enter four integers: 12 56 34 89

The greatest number is: 89


Result:
Thus, the program  that create a function to find the greatest number is verified successfully.


 
EXP NO:22 C PROGRAM TO PRINT THE MAXIMUM VALUES FOR THE AND, OR AND  XOR COMPARISONS
Aim:
To write a C program to print the maximum values for the AND, OR and XOR comparisons

Algorithm:
1.	Define a function calculate_the_max that takes two integers n and k as parameters.
2.	Declare variables a, o, and x to store the maximum values for AND, OR, and XOR operations, respectively.
3.	Use nested loops to iterate through pairs of integers (i, j) from 1 to n.
4.	Within the loops, check conditions for AND, OR, and XOR operations and update the corresponding maximum values (a, o, x).
5.	Declare variables n and k to store user input.
6.	Use scanf to take two integers as input.
7.	Call the calculate_the_max function with input values.
 
Program:
#include <stdio.h>

void calculate_the_max(int n, int k) {
    int a = 0, o = 0, x = 0;
    
    for (int i = 1; i < n; i++) {
        for (int j = i + 1; j <= n; j++) {
            if ((i & j) < k && (i & j) > a) {
                a = i & j;
            }
            if ((i | j) < k && (i | j) > o) {
                o = i | j;
            }
            if ((i ^ j) < k && (i ^ j) > x) {
                x = i ^ j;
            }
        }
    }
    
    printf("Maximum AND value: %d\n", a);
    printf("Maximum OR value: %d\n", o);
    printf("Maximum XOR value: %d\n", x);
}

int main() {
    int n, k;
    printf("Enter n and k: ");
    scanf("%d %d", &n, &k);
    
    calculate_the_max(n, k);
    
return 0;
}

Output:
Enter n and k: 5 6

Maximum AND value: 4

Maximum OR value: 5

Maximum XOR value: 5



Result:
Thus, the program to print the maximum values for the AND, OR and XOR comparisons
is verified successfully.


 
EXP NO:23 C PROGRAM TO WRITE THE LOGIC FOR THE REQUESTS
Aim:
To write a C program to write the logic for the requests

Algorithm:
1.	Declare variables noshel and noque to store the number of shelves and the number of queries, respectively.
2.	Use scanf to take two integers as input for the number of shelves and queries.
3.	Declare a 2D array shelarr to represent shelves and books, and an array nobookarr to store the number of books on each shelf.
4.	Declare variables k and c to keep track of the book index and the total number of books.
5.	Use a for loop to iterate over the queries.
 
Program:
#include <stdio.h>

int main() {
    int noshel, noque, k, c;
    printf("Enter number of shelves and queries: ");
    scanf("%d %d", &noshel, &noque);
    
    int shelarr[noshel][100], nobookarr[noshel];
    
    for (int i = 0; i < noshel; i++) {
        printf("Enter the number of books on shelf %d: ", i + 1);
        scanf("%d", &nobookarr[i]);
        
        printf("Enter books for shelf %d: ", i + 1);
        for (int j = 0; j < nobookarr[i]; j++) {
            scanf("%d", &shelarr[i][j]);
        }
    }
    
    printf("Enter the query number: ");
    scanf("%d", &noque);
    
    while (noque--) {
        printf("Enter shelf number and book index to find: ");
        scanf("%d %d", &k, &c);
        
        if (k - 1 < 0 || k - 1 >= noshel || c - 1 < 0 || c - 1 >= nobookarr[k - 1]) {
            printf("Invalid query\n");
        } else {
            printf("Book %d on shelf %d\n", shelarr[k - 1][c - 1], k);
        }
}
    
    return 0;
}


Output:
Enter number of shelves and queries: 2 2

Enter the number of books on shelf 1: 3

Enter books for shelf 1: 1 2 3

Enter the number of books on shelf 2: 2

Enter books for shelf 2: 4 5

Enter the query number: 2

Enter shelf number and book index to find: 1 2

Book 2 on shelf 1

Enter shelf number and book index to find: 2 1

Book 4 on shelf 2



Result:
Thus, the program to write the logic for the requests is verified successfully.


 
EXP NO:24 C PROGRAM PRINT THE SUM OF THE INTEGERS IN THE ARRAY.
Aim:
To write a C program print the sum of the integers in the array.

Algorithm:
1.	Declare a variable n to store the number of integers.
2.	Use scanf to take an integer n as input.
3.	Declare an array a of size n to store the integers.
4.	Declare a variable sum and initialize it to zero.
5.	Use a for loop to iterate n times:
6.	Use scanf to input each integer and add it to the sum.
7.	Print the final sum using printf.



Program:
#include <stdio.h>

int main() {
    int n, sum = 0;
    printf("Enter number of integers: ");
    scanf("%d", &n);
    
    int a[n];
    printf("Enter the integers:\n");
    for (int i = 0; i < n; i++) {
        scanf("%d", &a[i]);
        sum += a[i];
    }
    
    printf("Sum of the integers in the array: %d\n", sum);
    
    return 0;
}



Output:

Enter number of integers: 5

Enter the integers: 1 2 3 4 5

Sum of the integers in the array: 15



 


Result:
Thus, the program prints the sum of the integers in the array is verified successfully.


 
EXP NO 25: C PROGRAM TO COUNT THE NUMBER OF WORDS IN A      SENTENCE



Aim:

To write a C program that counts the number of words in a given sentence.

Algorithm:

1.	Input the sentence: Take a sentence from the user.
2.	Initialize a counter variable: This will keep track of the number of words.
3.	Process each character of the sentence:
o	Iterate through the sentence, checking each character.
o	If a character is not a space, it may belong to a word. If it's the first non-space character after a space or at the start, increment the word count.
4.	Handle spaces and punctuation: Skip over spaces, punctuation marks, and consider each word as a sequence of characters separated by spaces.
5.	Display the result: After processing the sentence, output the total word count.



Program:
#include <stdio.h>
#include <ctype.h>

int count_words(char *str) {
    int count = 0, in_word = 0;
    
    while (*str) {
        if (isspace(*str)) {
            in_word = 0;
        } else if (!in_word) {
            in_word = 1;
            count++;
        }
        str++;
    }
    
    return count;
}

int main() {
    char sentence[100];
    printf("Enter a sentence: ");
    fgets(sentence, sizeof(sentence), stdin);
    
    int word_count = count_words(sentence);
    printf("Number of words: %d\n", word_count);
    
    return 0;
}



Output:
Enter a sentence: Hello world this is C programming\

Number of words: 5




Result:

Thus, the program that counts the number of words in a given sentence is verified 
successfully.
