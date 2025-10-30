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

    int stack[40],top,i; void display()
    {
    for(i=top;i>=0;i--)
    {
    printf("%d\n",stack[i]);
    }
    }

  
Output:

<img width="245" height="444" alt="437743052-2a713552-ddf6-42ac-a265-ec997526d0cb" src="https://github.com/user-attachments/assets/1d10cdf6-ef6f-44a3-8229-0d45950b09e7" />




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

    int size=3,top=1; float stack[40];
    void push (float data)
    {
    if (top==size-1 )
    {
    printf("stack is full\n");
    }
    else
    {
    top ++; stack[top] = data;
    }
    }

Output:

<img width="461" height="392" alt="437743243-e3838830-dd79-413e-80d8-0db33e8a019b" src="https://github.com/user-attachments/assets/e8f7397f-f395-4f11-afa0-d4d369857486" />




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

    int queue[50], rear, front,i; void display()
    {
    if(front==-1)
    {
    printf("No elements to display");
    }
    else
    {
    for(i=front;i<=rear;i++)
    {
    printf("%d ",queue[i]);
    }
    }
    }

Output:

<img width="505" height="419" alt="437743577-2da5ab8c-fc0e-4715-9e44-065288f91ce8" src="https://github.com/user-attachments/assets/2d202970-5557-4903-a9c3-8315035cb2bc" />



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

    int size=4, rear=-1, front=-1; float queue[50];
    void enqueue(float data)
    {
    if(rear<size)
    {
    if(front==-1)
    {
    front=0;
    }
    rear=rear+1; queue[rear]=data;
    }
    }
    
Output:

<img width="571" height="307" alt="437743721-03fc86cd-3a06-433f-b8d9-55402b8b941d" src="https://github.com/user-attachments/assets/496cb64d-1d15-48d9-bab8-55d71ebb796b" />



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

    int front, rear;
    void dequeue()
    {
        if(front==-1&&rear==-1)
        printf("Queue Underflow.");
        else if(front==rear)
        front=rear=-1;
        else{
            front=front+1;
        }
    }

Output:


<img width="863" height="784" alt="437743988-329db24a-94a1-4e1d-b940-570adce9c368" src="https://github.com/user-attachments/assets/fd27c3dd-0e3c-4fb5-bd2f-271ea932dd59" />


Result:
Thus, the function that deletes an element from a queue implemented using an array is verified successfully.
