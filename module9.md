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
#include <stdio.h>
#define SIZE 5  // Define maximum size of the stack

int stack[SIZE];
int top = -1;

// Function to push an element into the stack
void push(int value) {
    if (top == SIZE - 1) {
        printf("Stack Overflow\n");
    } else {
        top++;
        stack[top] = value;
        printf("Pushed %d into the stack.\n", value);
    }
}

// Function to pop an element from the stack
void pop() {
    if (top == -1) {
        printf("Stack Underflow\n");
    } else {
        printf("Popped %d from the stack.\n", stack[top]);
        top--;
    }
}

// Function to display elements of the stack
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
                printf("Invalid choice! Try again.\n");
        }
    }
}



Output:

--- Stack Menu ---
1. Push
2. Pop
3. Display
4. Exit
Enter your choice: 1
Enter value to push: 10
Pushed 10 into the stack.

Enter your choice: 1
Enter value to push: 20
Pushed 20 into the stack.

Enter your choice: 3
Stack elements are:
20
10

Enter your choice: 2
Popped 20 from the stack.

Enter your choice: 3
Stack elements are:
10




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
#include <stdio.h>
#define SIZE 10  // Maximum size of the stack

float stack[SIZE];  // Stack array to hold float elements
int top = -1;       // Stack top initialized to -1 (empty stack)

// Function to push a float element into the stack
void push(float value) {
    if (top >= SIZE - 1) {
        printf("Stack Overflow! Cannot push %.2f\n", value);
    } else {
        top++;
        stack[top] = value;
        printf("Pushed %.2f into the stack.\n", value);
    }
}

// Main function
int main() {
    float value;
    int n, i;

    printf("Enter the number of elements to push: ");
    scanf("%d", &n);

    for (i = 0; i < n; i++) {
        printf("Enter element %d: ", i + 1);
        scanf("%f", &value);
        push(value);
    }

    return 0;
}




Output:


Enter the number of elements to push: 3
Enter element 1: 10.5
Pushed 10.50 into the stack.
Enter element 2: 20.25
Pushed 20.25 into the stack.
Enter element 3: 30.75
Pushed 30.75 into the stack.





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

#include <stdio.h>
#define SIZE 10  // Maximum size of the queue

int queue[SIZE];   // Queue array
int front = -1;    // Index of front element
int rear = -1;     // Index of rear element

// Function to enqueue an element
void enqueue(int value) {
    if (rear == SIZE - 1) {
        printf("Queue Overflow\n");
    } else {
        if (front == -1)
            front = 0;
        rear++;
        queue[rear] = value;
        printf("Enqueued %d into the queue.\n", value);
    }
}

// Function to dequeue an element
void dequeue() {
    if (front == -1 || front > rear) {
        printf("Queue Underflow\n");
    } else {
        printf("Dequeued %d from the queue.\n", queue[front]);
        front++;
    }
}

// Function to display queue elements
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
    int choice, value;

    while (1) {
        printf("\n--- Queue Menu ---\n");
        printf("1. Enqueue\n2. Dequeue\n3. Display\n4. Exit\n");
        printf("Enter your choice: ");
        scanf("%d", &choice);

        switch (choice) {
            case 1:
                printf("Enter value to enqueue: ");
                scanf("%d", &value);
                enqueue(value);
                break;
            case 2:
                dequeue();
                break;
            case 3:
                display();
                break;
            case 4:
                return 0;
            default:
                printf("Invalid choice! Try again.\n");
        }
    }
}


Output:

--- Queue Menu ---
1. Enqueue
2. Dequeue
3. Display
4. Exit
Enter your choice: 1
Enter value to enqueue: 10
Enqueued 10 into the queue.

Enter your choice: 1
Enter value to enqueue: 20
Enqueued 20 into the queue.

Enter your choice: 3
Queue elements are:
10 20

Enter your choice: 2
Dequeued 10 from the queue.

Enter your choice: 3
Queue elements are:
20



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

#include <stdio.h>
#define SIZE 10  // Define the maximum size of the queue

float queue[SIZE];  // Array to store float queue elements
int front = -1;     // Front index
int rear = -1;      // Rear index

// Function to insert a float element into the queue
void enqueue(float value) {
    if (rear == SIZE - 1) {
        printf("Queue Overflow! Cannot enqueue %.2f\n", value);
    } else {
        if (front == -1)  // First element insertion
            front = 0;
        rear++;
        queue[rear] = value;
        printf("Enqueued %.2f into the queue.\n", value);
    }
}

// Main function
int main() {
    int n;
    float value;

    printf("Enter the number of elements to enqueue: ");
    scanf("%d", &n);

    for (int i = 0; i < n; i++) {
        printf("Enter float element %d: ", i + 1);
        scanf("%f", &value);
        enqueue(value);
    }

    return 0;
}


Output:

Enter the number of elements to enqueue: 3
Enter float element 1: 10.5
Enqueued 10.50 into the queue.
Enter float element 2: 20.25
Enqueued 20.25 into the queue.
Enter float element 3: 30.75
Enqueued 30.75 into the queue.


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

#include <stdio.h>
#define SIZE 10  // Define maximum queue size

float queue[SIZE];  // Queue array for float values
int front = -1;     // Front index
int rear = -1;      // Rear index

// Function to enqueue a float element into the queue
void enqueue(float value) {
    if (rear == SIZE - 1) {
        printf("Queue Overflow! Cannot enqueue %.2f\n", value);
    } else {
        if (front == -1)  // First element insertion
            front = 0;
        rear++;
        queue[rear] = value;
        printf("Enqueued %.2f into the queue.\n", value);
    }
}

// Function to delete (dequeue) an element from the queue
void dequeue() {
    if (front == -1) {
        printf("Queue Underflow! Queue is empty.\n");
    } else {
        printf("Dequeued %.2f from the queue.\n", queue[front]);
        front++;

        // Reset if queue becomes empty
        if (front > rear) {
            front = -1;
            rear = -1;
        }
    }
}

// Function to display the queue
void display() {
    if (front == -1) {
        printf("Queue is empty.\n");
    } else {
        printf("Queue elements are:\n");
        for (int i = front; i <= rear; i++) {
            printf("%.2f ", queue[i]);
        }
        printf("\n");
    }
}

// Main function
int main() {
    enqueue(10.5);
    enqueue(20.25);
    enqueue(30.75);

    display();

    dequeue();  // Delete front element
    display();

    dequeue();
    dequeue();
    dequeue();  // Extra delete to show underflow

    return 0;
}


Output:

Enqueued 10.50 into the queue.
Enqueued 20.25 into the queue.
Enqueued 30.75 into the queue.
Queue elements are:
10.50 20.25 30.75 
Dequeued 10.50 from the queue.
Queue elements are:
20.25 30.75 
Dequeued 20.25 from the queue.
Dequeued 30.75 from the queue.
Queue Underflow! Queue is empty.



Result:
Thus, the function that deletes an element from a queue implemented using an array is verified successfully.
