EXP NO:11 C PROGRAM TO DISPLAY STACK ELEMENTS USING AN ARRAY.

Aim:
To write a C program to display stack elements using an array.
Algorithm:
1.	Include Necessary Header Files
2.	Declare Global Variables
3.	Define the Display Function
4.	Main Function (or Other Relevant Code)
5.	Initialize the stack and top as needed.
6.	Perform stack operations (push, pop, etc.).
7.	Use the display function to visualize the stack's contents
 
Program:

//type your code here
#include <stdio.h>
#define SIZE 100

int stack[SIZE];
int top = -1;

// Function to push element onto stack
void push(int value) {
    if (top == SIZE - 1) {
        printf("Stack Overflow\n");
    } else {
        stack[++top] = value;
        printf("%d pushed into stack.\n", value);
    }
}

// Function to pop element from stack
void pop() {
    if (top == -1) {
        printf("Stack Underflow\n");
    } else {
        printf("%d popped from stack.\n", stack[top--]);
    }
}

// Function to display the stack
void display() {
    if (top == -1) {
        printf("Stack is empty.\n");
    } else {
        printf("Stack elements are:\n");
        for (int i = top; i >= 0; i--) {
            printf("%d\n", stack[i]);
        }
    }
}

// Main function
int main() {
    int choice, value;

    while (1) {
        printf("\n--- Stack Menu ---\n");
        printf("1. Push\n2. Pop\n3. Display\n4. Exit\n");
        printf("Enter your choice: ");
        scanf("%d", &choice);

        switch (choice) {
        case 1:
            printf("Enter value to push: ");
            scanf("%d", &value);
            push(value);
            break;
        case 2:
            pop();
            break;
        case 3:
            display();
            break;
        case 4:
            return 0;
        default:
            printf("Invalid choice.\n");
        }
    }

    return 0;
}


Output:

//paste your output here
--- Stack Menu ---
1. Push
2. Pop
3. Display
4. Exit
Enter your choice: 1
Enter value to push: 10
10 pushed into stack.

--- Stack Menu ---
1. Push
2. Pop
3. Display
4. Exit
Enter your choice: 1
Enter value to push: 20
20 pushed into stack.

--- Stack Menu ---
1. Push
2. Pop
3. Display
4. Exit
Enter your choice: 1
Enter value to push: 30
30 pushed into stack.

--- Stack Menu ---
1. Push
2. Pop
3. Display
4. Exit
Enter your choice: 3
Stack elements are:
30
20
10

--- Stack Menu ---
1. Push
2. Pop
3. Display
4. Exit
Enter your choice: 2
30 popped from stack.

--- Stack Menu ---
1. Push
2. Pop
3. Display
4. Exit
Enter your choice: 3
Stack elements are:
20
10

--- Stack Menu ---
1. Push
2. Pop
3. Display
4. Exit
Enter your choice: 4




Result:
Thus, the program to display stack elements using an array is verified successfully.
 

EXP NO:12  PROGRAM TO PUSH THE GIVEN ELEMENT IN TO A STACK USING ARRAY.
Aim:
To create a C program to push the given element in to a stack using array.
Algorithm:
1.	Declare global variables for the stack size, top index, and the stack itself.
2.	Define the push function to add a floating-point number to the stack.
3.	Initialize the stack size, top index, and the stack itself.
4.	Call the push function as needed.
 
Program:

//type your code here
#include <stdio.h>
#define SIZE 100

float stack[SIZE];
int top = -1;

// Function to push a float element into the stack
void push(float value) {
    if (top == SIZE - 1) {
        printf("Stack Overflow! Cannot push %.2f\n", value);
    } else {
        top++;
        stack[top] = value;
        printf("%.2f pushed into the stack.\n", value);
    }
}

// Main function
int main() {
    int n, i;
    float value;

    printf("Enter the number of elements to push into the stack: ");
    scanf("%d", &n);

    for (i = 0; i < n; i++) {
        printf("Enter element %d: ", i + 1);
        scanf("%f", &value);
        push(value);
    }

    return 0;
}

Output:

//paste your output here
Enter the number of elements to push into the stack: 3
Enter element 1: 10.5
10.50 pushed into the stack.
Enter element 2: 20.75
20.75 pushed into the stack.
Enter element 3: 30.25
30.25 pushed into the stack.





Result:
Thus, the program to push the given element in to a stack using array is verified successfully


 
EXP NO:13 C PROGRAM TO DISPLAY QUEUE ELEMENTS USING ARRAY.
Aim:
To write a C program to display queue elements using array

Algorithm:
1.	Declare global variables for the queue, rear, front, and iteration.
2.	Define the display function to print the elements of the queue.
3.	Initialize the queue, rear, and front as needed.
4.	Call the display function and perform other queue operations as needed.
 
Program:

//type your code here
#include <stdio.h>
#define SIZE 100

int queue[SIZE];
int front = -1, rear = -1;

// Function to insert an element into the queue
void enqueue(int value) {
    if (rear == SIZE - 1) {
        printf("Queue Overflow!\n");
    } else {
        if (front == -1) front = 0;  // First element
        queue[++rear] = value;
        printf("%d enqueued into the queue.\n", value);
    }
}

// Function to display elements of the queue
void display() {
    if (front == -1 || front > rear) {
        printf("Queue is empty.\n");
    } else {
        printf("Queue elements are:\n");
        for (int i = front; i <= rear; i++) {
            printf("%d ", queue[i]);
        }
        printf("\n");
    }
}

// Main function
int main() {
    int n, value;

    printf("Enter number of elements to enqueue: ");
    scanf("%d", &n);

    for (int i = 0; i < n; i++) {
        printf("Enter element %d: ", i + 1);
        scanf("%d", &value);
        enqueue(value);
    }

    // Display queue elements
    display();

    return 0;
}

Output:

//paste your output here
Enter number of elements to enqueue: 4
Enter element 1: 10
10 enqueued into the queue.
Enter element 2: 20
20 enqueued into the queue.
Enter element 3: 30
30 enqueued into the queue.
Enter element 4: 40
40 enqueued into the queue.
Queue elements are:
10 20 30 40



Result:
Thus, the program to display queue elements using array is verified successfully.


 
EXP NO:14 C PROGRAM TO INSERT ELEMENTS IN QUEUE USING ARRAY.
Aim:
To write a C program to insert elements in queue using array.

Algorithm:
1.	Declare global variables for the size, rear, front, and the queue itself.
2.	Define the enqueue function to add a float to the queue.
3.	Initialize the rear, front, and size of the queue as needed.
4.	Call the enqueue function as needed.

Program:

//type your code here
#include <stdio.h>
#define SIZE 100

float queue[SIZE];
int front = -1, rear = -1;

// Function to insert (enqueue) a float element into the queue
void enqueue(float value) {
    if (rear == SIZE - 1) {
        printf("Queue Overflow! Cannot enqueue %.2f\n", value);
    } else {
        if (front == -1) front = 0;  // First insertion
        queue[++rear] = value;
        printf("%.2f enqueued into the queue.\n", value);
    }
}

// Main function
int main() {
    int n;
    float value;

    printf("Enter the number of float elements to insert into the queue: ");
    scanf("%d", &n);

    for (int i = 0; i < n; i++) {
        printf("Enter element %d: ", i + 1);
        scanf("%f", &value);
        enqueue(value);
    }

    return 0;
}


Output:

//paste your output here
Enter the number of float elements to insert into the queue: 3
Enter element 1: 12.5
12.50 enqueued into the queue.
Enter element 2: 23.75
23.75 enqueued into the queue.
Enter element 3: 45.10
45.10 enqueued into the queue.


Result:
Thus, the program to insert elements in queue using array is verified successfully.



 
EXP NO:15 C FUNCTION TO DELETE ELEMENTS IN QUEUE USING ARRAY



Aim:

To create a function in C that deletes an element from a queue implemented using an array.

Algorithm:

1.	Check if the Queue is Empty
o	If the front pointer is -1, it means the queue is empty, and there are no elements to delete. Print a message indicating that the queue is empty.
2.	Delete the Front Element
o	If the queue is not empty, the element at the front index is deleted.
o	Increment the front pointer by 1 to remove the element and point to the next element in the queue.
3.	Check if the Queue Becomes Empty After Deletion:
o	After deletion, check if the front pointer has passed the rear pointer (front > rear). If this is true, reset both front and rear to -1, indicating that the queue is now empty.
4.	End the Function.



Program:

//type your code here
#include <stdio.h>
#define SIZE 100

int queue[SIZE];
int front = -1, rear = -1;

// Function to delete (dequeue) an element from the queue
void dequeue() {
    if (front == -1) {
        printf("Queue Underflow! Queue is empty.\n");
    } else {
        printf("Element %d deleted from the queue.\n", queue[front]);
        front++;

        // If queue becomes empty after deletion
        if (front > rear) {
            front = rear = -1;
        }
    }
}

// Function to insert elements into the queue (for testing)
void enqueue(int value) {
    if (rear == SIZE - 1) {
        printf("Queue Overflow! Cannot enqueue %d\n", value);
    } else {
        if (front == -1) front = 0;
        queue[++rear] = value;
        printf("%d enqueued into the queue.\n", value);
    }
}

// Function to display elements of the queue
void display() {
    if (front == -1 || front > rear) {
        printf("Queue is empty.\n");
    } else {
        printf("Queue elements are:\n");
        for (int i = front; i <= rear; i++) {
            printf("%d ", queue[i]);
        }
        printf("\n");
    }
}

// Main function
int main() {
    enqueue(10);
    enqueue(20);
    enqueue(30);
    display();

    dequeue();
    display();

    dequeue();
    dequeue();
    dequeue(); // Extra dequeue to show underflow

    return 0;
}


Output:

//paste your output here
10 enqueued into the queue.
20 enqueued into the queue.
30 enqueued into the queue.
Queue elements are:
10 20 30
Element 10 deleted from the queue.
Queue elements are:
20 30
Element 20 deleted from the queue.
Element 30 deleted from the queue.
Queue Underflow! Queue is empty.



Result:
Thus, the function that deletes an element from a queue implemented using an array is verified successfully.
