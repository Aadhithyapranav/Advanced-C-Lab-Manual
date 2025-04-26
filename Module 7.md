EXP NO:1 C PROGRAM FOR ARRAY OF STRUCTURE TO CHECK ELIGIBILITY FOR THE VACCINE.

Aim:
To write a C program for array of structure to check eligibility for the vaccine person age above 6 years of age.

Algorithm:
1.	Declare structure eligible with age (integer) and n (character array)
2.	Declare variable e of type eligible
3.	Input age and name using scanf, store in e
4.	If e.age <= 6
-	Print "Vaccine Eligibility: No"
Else
-	Print "Vaccine Eligibility: Yes"
5.	Print details (e.age, e.n)
6.	Return 0
 
Program:

//type your code here
#include <stdio.h>
#include <string.h>

// Step 1: Declare structure
struct eligible {
    int age;
    char name[50];
};

int main() {
    // Step 2: Declare variables
    int i, n;
    printf("Enter the number of persons: ");
    scanf("%d", &n);

    struct eligible e[n];  // Array of structures

    // Step 3: Input details
    for(i = 0; i < n; i++) {
        printf("\nEnter name of person %d: ", i + 1);
        scanf("%s", e[i].name);
        printf("Enter age of %s: ", e[i].name);
        scanf("%d", &e[i].age);
    }

    // Step 4 & 5: Check eligibility and print details
    printf("\n--- Vaccine Eligibility Status ---\n");
    for(i = 0; i < n; i++) {
        printf("Name: %s\n", e[i].name);
        printf("Age: %d\n", e[i].age);
        if(e[i].age <= 6) {
            printf("Vaccine Eligibility: No\n");
        } else {
            printf("Vaccine Eligibility: Yes\n");
        }
        printf("----------------------------\n");
    }

    // Step 6: End of program
    return 0;
}



Output:

//paste your output here
Enter the number of persons: 3

Enter name of person 1: Alice
Enter age of Alice: 5

Enter name of person 2: Bob
Enter age of Bob: 10

Enter name of person 3: Charlie
Enter age of Charlie: 6

--- Vaccine Eligibility Status ---
Name: Alice
Age: 5
Vaccine Eligibility: No
----------------------------
Name: Bob
Age: 10
Vaccine Eligibility: Yes
----------------------------
Name: Charlie
Age: 6
Vaccine Eligibility: No
----------------------------


Result:
Thus, the program is verified successfully. 



EXP NO:2 C PROGRAM FOR PASSING STRUCTURES AS FUNCTION ARGUMENTS AND RETURNING A STRUCTURE FROM A FUNCTION
Aim:
To write a C program for passing structure as function and returning a structure from a function

Algorithm:
1.	Define structure numbers with members a and b.
2.	Declare variable n of type numbers.
3.	Prompt the user to enter values for a and b.
4.	Input values for a and b into n using scanf.
5.	Call the add function with n as an argument.
6.	Print the result returned by the add function.
7.	Return 0
 
Program:

//type your code here
#include <stdio.h>

// Step 1: Define structure
struct numbers {
    int a;
    int b;
};

// Function to add two numbers from structure
struct numbers add(struct numbers n) {
    struct numbers result;
    result.a = n.a + n.b;  // sum stored in a
    return result;
}

int main() {
    // Step 2: Declare structure variable
    struct numbers n, res;

    // Step 3 & 4: Get user input
    printf("Enter value of a: ");
    scanf("%d", &n.a);
    printf("Enter value of b: ");
    scanf("%d", &n.b);

    // Step 5: Call function
    res = add(n);

    // Step 6: Print result
    printf("Sum: %d\n", res.a);

    // Step 7: Return
    return 0;
}






Output:


//paste your output here
Enter value of a: 7
Enter value of b: 8
Sum: 15





Result:
Thus, the program is verified successfully


 
EXP.NO:3 C PROGRAM TO READ A FILE NAME FROM USER AND WRITE THAT FILE USING FOPEN()

Aim:
To write a C program to read a file name from user

Algorithm:
1.	Include the necessary header file stdio.h.
2.	Begin the main function.
3.	Declare a file pointer p.
Declare a character array name to store the file name.
4.	Prompt the user to enter a file name.
Use scanf to input the file name into the name array.
5.	Print a message indicating that the file with the specified name has been created successfully.
6.	Use fopen to open a file with the name provided by the user in write mode ("w").
-	If successful, continue to the next step.
-	If unsuccessful, print an error message and exit the program with a non-zero status.
1.	Print a message indicating that the file has been opened successfully.
2.	Use fclose to close the file.
3.	Print a message indicating that the file has been closed.
4.	End the main function.
5.	Return 0 to indicate successful program execution.
 
Program:

//type your code here
#include <stdio.h>  // Step 1

int main() {        // Step 2
    FILE *p;        // Step 3: File pointer
    char name[100]; // Character array to store file name

    // Step 4: Prompt user
    printf("Enter the file name to create: ");
    scanf("%s", name);  // Read file name

    // Step 5: Show message
    printf("Creating file: %s\n", name);

    // Step 6: Open file in write mode
    p = fopen(name, "w");
    if (p == NULL) {
        printf("Error: Could not create file.\n");
        return 1;  // Exit with non-zero status
    }

    // Step 7: File opened successfully
    printf("File opened successfully.\n");

    // Step 8: Close the file
    fclose(p);

    // Step 9: File closed message
    printf("File closed.\n");

    // Step 10: End of program
    return 0;
}





Output:


//paste your output here
Enter the file name to create: testfile.txt
Creating file: testfile.txt
File opened successfully.
File closed.












Result:
Thus, the program is verified successfully
 


EXP NO:4   PROGRAM TO READ A FILE NAME FROM USER, WRITE THAT FILE AND INSERT TEXT IN TO THAT FILE
Aim:
To write a C program to read, a file and insert text in that file
Algorithm:
1.	Include the necessary header file stdio.h.
2.	Begin the main function.
3.	Declare a file pointer p.
Declare character arrays name and text. Declare an integer variable num.
4.	Prompt the user to enter a file name and the number of strings.
Use scanf to input the file name into the name array and the number of strings into the num variable.
5.	Use fopen to open a file with the name provided by the user in write mode ("w").
-	If successful, continue to the next step.
-	If unsuccessful, print an error message and exit the program with a non-zero status.
6.	Print a message indicating that the file has been opened successfully.
1.	Use a loop to input strings from the user and write them to the file using fputs.
2.	Use fclose to close the file.
3.	Print a message indicating that data has been added successfully.
4.	End the main function.
5.	Return 0 to indicate successful program execution.
 
Program:

//type your code here
#include <stdio.h>   // Step 1

int main() {         // Step 2
    FILE *p;         // Step 3: Declare file pointer
    char name[100], text[200];
    int num;

    // Step 4: Get file name and number of lines
    printf("Enter the file name to write into: ");
    scanf("%s", name);
    printf("Enter the number of lines to insert: ");
    scanf("%d", &num);

    // Clear input buffer before using fgets
    getchar();

    // Step 5: Open file in write mode
    p = fopen(name, "w");
    if (p == NULL) {
        printf("Error: Could not open file.\n");
        return 1;
    }

    // Step 6: File opened message
    printf("File opened successfully.\n");

    // Step 7: Loop to get strings and write them to file
    for (int i = 0; i < num; i++) {
        printf("Enter line %d: ", i + 1);
        fgets(text, sizeof(text), stdin);  // Read a line with spaces
        fputs(text, p);                    // Write to file
    }

    // Step 8: Close the file
    fclose(p);

    // Step 9: Success message
    printf("Data added to the file successfully.\n");

    // Step 10: End of program
    return 0;
}





Output:


//paste your output here
Enter the file name to write into: mynotes.txt
Enter the number of lines to insert: 2
File opened successfully.
Enter line 1: C is a powerful language.
Enter line 2: File handling is very useful.
Data added to the file successfully.







Result:
Thus, the program is verified successfully



Ex No 5 : C PROGRAM TO DISPLAY STUDENT DETAILS USING STRUCTURE


10.Free the allocated memory

11.After all operations are done, call free(s) to release the dynamically allocated memory.

12.Return from the main function

13.End the program by returning 0.
Aim:
The aim of this program is to dynamically allocate memory to store information about multiple subjects (name and marks), input the details for each subject, and then display the stored information. Finally, it frees the allocated memory to prevent memory leaks.

Algorithm:
1.Input the number of subjects.

2.Read the integer value n from the user, which represents the number of subjects.

3.Dynamically allocate memory:

4.Use malloc to allocate memory for n subjects. Each subject has a name (array of characters) and marks (integer).

5.If memory allocation fails (i.e., the pointer s is NULL), display an error message and exit the program.

6.Input the details of each subject

7.Use a for loop to read the name and marks of each subject using scanf. For each subject, store the name as a string and marks as an integer in the dynamically allocated memory.

8.Display the details of each subject

9.Use another for loop to print the name and marks of each subject.

Program:

//type your code here

#include <stdio.h>
#include <stdlib.h>  // for malloc and free

// Define structure to hold subject details
struct subject {
    char name[50];
    int marks;
};

int main() {
    int n, i;
    struct subject *s;

    // Step 1 & 2: Input number of subjects
    printf("Enter the number of subjects: ");
    scanf("%d", &n);

    // Step 3 & 4: Dynamically allocate memory
    s = (struct subject *)malloc(n * sizeof(struct subject));

    // Step 5: Check memory allocation
    if (s == NULL) {
        printf("Memory allocation failed.\n");
        return 1;
    }

    // Step 6 & 7: Input subject details
    for (i = 0; i < n; i++) {
        printf("Enter name of subject %d: ", i + 1);
        scanf("%s", s[i].name);
        printf("Enter marks for %s: ", s[i].name);
        scanf("%d", &s[i].marks);
    }

    // Step 8 & 9: Display subject details
    printf("\n--- Subject Details ---\n");
    for (i = 0; i < n; i++) {
        printf("Subject %d: %s, Marks: %d\n", i + 1, s[i].name, s[i].marks);
    }

    // Step 10: Free dynamically allocated memory
    free(s);

    return 0;
}





Output:


//paste your output here
Enter the number of subjects: 2
Enter name of subject 1: Math
Enter marks for Math: 95
Enter name of subject 2: English
Enter marks for English: 88

--- Subject Details ---
Subject 1: Math, Marks: 95
Subject 2: English, Marks: 88







Result:
Thus, the program is verified successfully
