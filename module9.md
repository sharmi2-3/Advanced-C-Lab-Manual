**EXP NO:11 C PROGRAM TO DISPLAY STACK ELEMENTS USING AN ARRAY.**

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

```
#include <stdio.h>
#define MAX 5

int stack[MAX];
int top = -1;

void push(int value)
{
    if(top == MAX - 1)
    {
        printf("Stack Overflow\n");
    }else{
        top++;
        stack[top] = value;
    }
}

void display()
{
    int i;

    if(top == -1)
    {
        printf("Stack is Empty\n");
    }
    else
    {
        printf("Stack Elements are:\n");

        for(i = top; i >= 0; i--)
        {
            printf("%d\n", stack[i]);
        }
    }
}

int main()
{
    int n, i, value;

    printf("Enter number of elements: ");
    scanf("%d", &n);

    printf("Enter stack elements:\n");

    for(i = 0; i < n; i++)
    {
        scanf("%d", &value);
        push(value);
    }

    display();

    return 0;
}
```

Output:

<img width="1516" height="1050" alt="image" src="https://github.com/user-attachments/assets/afdbd093-3cd0-4f03-8dc1-2718bd6fd0f1" />



Result:

Thus, the program to display stack elements using an array is verified successfully.
 

**EXP NO:12  PROGRAM TO PUSH THE GIVEN ELEMENT IN TO A STACK USING ARRAY.**

Aim:

To create a C program to push the given element in to a stack using array.

Algorithm:

1.	Declare global variables for the stack size, top index, and the stack itself.
2.	Define the push function to add a floating-point number to the stack.
3.	Initialize the stack size, top index, and the stack itself.
4.	Call the push function as needed.
 
Program:
```
#include <stdio.h>

#define MAX 5

int stack[MAX];
int top = -1;

void push(int value)
{
    if(top == MAX - 1)
    {
        printf("Stack Overflow\n");
    }
    else
    {
        top++;
        stack[top] = value;
        printf("%d pushed into stack\n", value);
    }
}

void display()
{
    int i;

    if(top == -1)
    {
        printf("Stack is Empty\n");
    }
    else
    {
        printf("Stack elements are:\n");

        for(i = top; i >= 0; i--)
        {
            printf("%d\n", stack[i]);
        }
    }
}

int main()
{
    int value;

    printf("Enter the element to push: ");
    scanf("%d", &value);

    push(value);

    display();

    return 0;
}
```

Output:

<img width="1337" height="1045" alt="image" src="https://github.com/user-attachments/assets/2278db8b-ff7c-446f-9a33-054921b78b17" />


Result:

Thus, the program to push the given element in to a stack using array is verified successfully


 
**EXP NO:13 C PROGRAM TO DISPLAY QUEUE ELEMENTS USING ARRAY.**

Aim:

To write a C program to display queue elements using array

Algorithm:

1.	Declare global variables for the queue, rear, front, and iteration.
2.	Define the display function to print the elements of the queue.
3.	Initialize the queue, rear, and front as needed.
4.	Call the display function and perform other queue operations as needed.
 
Program:

```
#include <stdio.h>
#define MAX 5

int queue[MAX];
int front = -1;
int rear = -1;

void insert(int value)
{
    if(rear == MAX - 1){
        printf("Queue Overflow\n");
    }else{
        if(front == -1){
            front = 0;
        }

        rear++;
        queue[rear] = value;
    }
}

void display()
{
    int i;

    if(front == -1 || front > rear){
        printf("Queue is Empty\n");
    }else{
        printf("Queue elements are:\n");

        for(i = front; i <= rear; i++){
            printf("%d\n", queue[i]);
        }
    }
}

int main()
{
    int n, i, value;

    printf("Enter number of elements: ");
    scanf("%d", &n);

    printf("Enter queue elements:\n");

    for(i = 0; i < n; i++){
        scanf("%d", &value);
        insert(value);
    }

    display();

    return 0;
}
```

Output:

<img width="1349" height="1046" alt="image" src="https://github.com/user-attachments/assets/537666b1-40f5-4358-aa48-4ba643d13d0c" />



Result:

Thus, the program to display queue elements using array is verified successfully.


 
**EXP NO:14 C PROGRAM TO INSERT ELEMENTS IN QUEUE USING ARRAY.**

Aim:

To write a C program to insert elements in queue using array.

Algorithm:

1.	Declare global variables for the size, rear, front, and the queue itself.
2.	Define the enqueue function to add a float to the queue.
3.	Initialize the rear, front, and size of the queue as needed.
4.	Call the enqueue function as needed.

Program:
```
#include <stdio.h>
#define MAX 5

int queue[MAX];
int front = -1;
int rear = -1;

void enqueue(int value)
{
    if(rear == MAX - 1){
        printf("Queue Overflow\n");
    }else{
        if(front == -1){
            front = 0;
        }

        rear++;
        queue[rear] = value;

        printf("%d inserted into queue\n", value);
    }
}

void display()
{
    int i;

    if(front == -1){
        printf("Queue is Empty\n");
    }else{
        printf("Queue elements are:\n");

        for(i = front; i <= rear; i++){
            printf("%d\n", queue[i]);
        }
    }
}

int main()
{
    int value;

    printf("Enter the element to insert: ");
    scanf("%d", &value);

    enqueue(value);

    display();

    return 0;
}
```

Output:

<img width="1407" height="1049" alt="image" src="https://github.com/user-attachments/assets/b3b6a67c-e005-423f-8954-594d05cdca2e" />


Result:

Thus, the program to insert elements in queue using array is verified successfully.



 
**EXP NO:15 C FUNCTION TO DELETE ELEMENTS IN QUEUE USING ARRAY**



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
```
#include <stdio.h>
#define MAX 5

int queue[MAX];
int front = -1;
int rear = -1;

void enqueue(int value)
{
    if(rear == MAX - 1){
        printf("Queue Overflow\n");
    }else{
        if(front == -1){
            front = 0;
        }

        rear++;
        queue[rear] = value;
    }
}
void dequeue()
{
    if(front == -1){
        printf("Queue Underflow\n");
    }else{
        printf("Deleted element is %d\n", queue[front]);
        front++;

        if(front > rear){
            front = rear = -1;
        }
    }
}
void display()
{
    int i;

    if(front == -1){
        printf("Queue is Empty\n");
    }else{
        printf("Remaining queue elements are:\n");

        for(i = front; i <= rear; i++){
            printf("%d\n", queue[i]);
        }
    }
}
int main()
{
    enqueue(10);
    enqueue(20);
    enqueue(30);

    dequeue();

    display();

    return 0;
}
```
Output:

<img width="1411" height="1055" alt="image" src="https://github.com/user-attachments/assets/de690aba-f6e3-4680-bf3c-a892db9976a5" />



Result:
Thus, the function that deletes an element from a queue implemented using an array is verified successfully.
