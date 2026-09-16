

**EXP NO 26: C PROGRAM TO DISPLAY STACK ELEMENTS USING LINKED LIST.**

Aim:

To write a C program to display stack elements using linked list.

Algorithm:

1.	Define a structure Node with two members: data to store the integer value and next to point to the next node in the linked list.
2.	Declare a global variable head representing the starting node of the linked list.
3.	Define a function display to print the elements of the linked list.
4.	Declare a pointer p and initialize it with the head of the linked list.
5.	Use a while loop to traverse the linked list:
6.	Print the data of the current node.
7.	Move to the next node using the next pointer.
 
Program:

```
#include <stdio.h>
#include <stdlib.h>

struct Node
{
    int data;
    struct Node *next;
};
struct Node *head = NULL;

void push(int value)
{
    struct Node *newnode;
    newnode = (struct Node *)malloc(sizeof(struct Node));
    newnode->data = value;
    newnode->next = head;
    head = newnode;
}

void display()
{
    struct Node *p;
    p = head;

    printf("Stack elements are:\n");

    while(p != NULL){
        printf("%d\n", p->data);
        p = p->next;
    }
}

int main()
{
    push(10);
    push(20);
    push(30);

    display();

    return 0;
}
```

Output:

<img width="1346" height="1048" alt="image" src="https://github.com/user-attachments/assets/a31922e6-56dc-47b7-a7db-cdec2b2f68e1" />



Result:

Thus, the program to display stack elements using linked list is verified successfully. 



**EXP.NO 27: C PROGRAM TO POP AN ELEMENT FROM THE GIVEN STACK USING 
LINKED LIST.**

Aim:

To write a C program to pop an element from the given stack using liked list.

Algorithm:

1.	Check for Empty Stack
2.	If head is equal to NULL, Print "Stack is empty."
3.	Else Proceed to the next step.
4.	Set head to point to the next node in the stack.
 
Program:

```
#include <stdio.h>
#include <stdlib.h>

struct Node
{
    int data;
    struct Node *next;
};
struct Node *head = NULL;

void push(int value)
{
    struct Node *newnode;
    newnode = (struct Node *)malloc(sizeof(struct Node));
    newnode->data = value;
    newnode->next = head;
    head = newnode;
}
void pop()
{
    struct Node *temp;
    if(head == NULL){
        printf("Stack is empty\n");
    }else{
        temp = head;
        printf("Deleted element = %d\n", head->data);
        head = head->next;
        free(temp);
    }
}
void display()
{
    struct Node *p = head;
    printf("Stack elements are:\n");

    while(p != NULL){
        printf("%d\n", p->data);
        p = p->next;
    }
}
int main()
{
    push(10);
    push(20);
    push(30);

    pop();
    display();

    return 0;
}
```

Output:

<img width="1348" height="1045" alt="image" src="https://github.com/user-attachments/assets/dd5344e7-b1e2-41b8-bc40-a9b457776335" />


Result:

Thus, the program to pop an element from the given stack using liked list is verified successfully.

 
**EXP NO:28 C PROGRAM TO DISPLAY QUEUE ELEMENTS USING LINKED LIST.**

Aim:

To write a C program to display queue elements using linked list.

Algorithm:

1.	Check if Queue is Empty
2.	Display Queue Elements
3.	Print the data of the current node pointed to by front
4.	Update front to point to the next node.
5.	End the display function.
 
Program:

```
#include <stdio.h>
#include <stdlib.h>

struct Node
{
    int data;
    struct Node *next;
};
struct Node *front = NULL;
struct Node *rear = NULL;

void enqueue(int value)
{
    struct Node *newnode;
    newnode = (struct Node *)malloc(sizeof(struct Node));
    newnode->data = value;
    newnode->next = NULL;

    if(rear == NULL){
        front = rear = newnode;
    }else{
        rear->next = newnode;
        rear = newnode;
    }
}
void display()
{
    struct Node *temp;
    if(front == NULL){
        printf("Queue is empty\n");
    }else{
        temp = front;
        printf("Queue elements are:\n");
        while(temp != NULL){
            printf("%d\n", temp->data);
            temp = temp->next;
        }
    }
}
int main()
{
    enqueue(10);
    enqueue(20);
    enqueue(30);

    display();

    return 0;
}
```

Output:

<img width="1356" height="1053" alt="image" src="https://github.com/user-attachments/assets/10235916-7e8e-4628-aae3-f625ff1daa0d" />


Result:

Thus, the program to display queue elements using linked list is verified successfully.


**EXP NO:29 C PROGRAM TO INSERT ELEMENTS IN QUEUE USING LINKED LIST**

Aim:

To write a C program to insert elements in queue using linked list

Algorithm:

1.	Allocate Memory for New Node
2.	Set Data and Next Pointer
3.	Check if Queue is Empty
4.	Set both front and rear to point to the new node p.
5.	Set the next pointer of the current rear to point to the new node p.
6.	End of Enqueue Operation
 
Program:
```
#include <stdio.h>
#include <stdlib.h>

struct Node
{
    int data;
    struct Node *next;
};
struct Node *front = NULL;
struct Node *rear = NULL;

void enqueue(int value)
{
    struct Node *p;
    p = (struct Node *)malloc(sizeof(struct Node));
    p->data = value;
    p->next = NULL;
    
    if(front == NULL && rear == NULL){
        front = rear = p;
    }else{
        rear->next = p;
        rear = p;
    }
}
void display()
{
    struct Node *temp;
    temp = front;
    printf("Queue elements are:\n");

    while(temp != NULL){
        printf("%d\n", temp->data);
        temp = temp->next;
    }
}
int main()
{
    enqueue(10);
    enqueue(20);
    enqueue(30);

    display();

    return 0;
}
```

Output:

<img width="1415" height="1016" alt="image" src="https://github.com/user-attachments/assets/89c5d2a7-06d8-4303-968a-4e2fe6beb5de" />


Result:

Thus, the program to insert elements in queue using linked list is verified successfully.



**EXP NO:30 C FUNCTION TO FIND THE PEEK OF QUEUE USING LINKED LIST.**


Aim:

The aim of this function is to retrieve the "peek" (the front element) of a queue implemented using a linked list

Algorithm:

1.	Check if the queue is empty:
o	If the queue is empty (i.e., the front pointer is NULL), return an error or a message indicating that the queue is empty.
2.	Access the front element:
o	If the queue is not empty, return the data stored in the front node of the linked list (i.e., the element at the head of the queue).

Program:

```
#include <stdio.h>
#include <stdlib.h>

struct Node
{
    int data;
    struct Node *next;
};
struct Node *front = NULL;
struct Node *rear = NULL;

void enqueue(int value)
{
    struct Node *newnode;
    newnode = (struct Node *)malloc(sizeof(struct Node));
    newnode->data = value;
    newnode->next = NULL;

    if(front == NULL && rear == NULL){
        front = rear = newnode;
    }else{
        rear->next = newnode;
        rear = newnode;
    }
}
void peek()
{
    if(front == NULL){
        printf("Queue is empty\n");
    }else{
        printf("Front element = %d\n", front->data);
    }
}

int main()
{
    enqueue(10);
    enqueue(20);
    enqueue(30);

    peek();

    return 0;
}
```

Output:

<img width="1426" height="1037" alt="image" src="https://github.com/user-attachments/assets/36d76e2b-503d-4a1b-94cb-099916c09dff" />



Result:

Thus, the program to retrieve the "peek" (the front element) of a queue implemented using a linked list is verified successfully.


