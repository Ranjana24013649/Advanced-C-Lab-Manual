EXP NO:16 C PROGRAM TO SEARCH A GIVEN ELEMENT IN THE GIVEN LINKED LIST.
Aim:
To write a C program to search a given element in the given linked list.

Algorithm:
1.	Define the structure for a node in a linked list.
2.	Define the search function to find a specific character in the linked list.
3.	Initialize the head of the linked list as needed.
4.	Call the search function and perform other linked list operations as needed.
 
Program:

    struct Node *next; char data;
    }*head;
    void search(char data)
    {
    struct Node *ptr; char item=data; int i=0,flag;
    ptr = head; if(ptr == NULL)
    {
    printf("Empty List\n");
    }
    else
    {
    while (ptr!=NULL)
    {
    if(ptr->data == item)
    {
    printf("item %c found at location %d ",item,i+1); flag=0;
    }
    i++;
    ptr = ptr -> next;
    }
    if(flag!=0)
    {
    printf("Item not found\n");
    }
    }
    
    }

Output:

<img width="604" height="423" alt="437745345-ba7f8391-a4a0-4869-a27d-bfdd11fdcaca" src="https://github.com/user-attachments/assets/0090421d-b014-4701-a35b-af64dcf81dcf" />




Result:
Thus, the program to search a given element in the given linked list is verified successfully.


 
EXP NO:17  PROGRAM TO INSERT A NODE IN A LINKED LIST.
Aim:
To write a C program to insert a node in a linked list.
Algorithm:
1.	Define the structure for a node in a linked list
2.	Define the insert function to insert a new node with character data at the end of the linked list.
3.	Initialize the head of the linked list as needed.
4.	Call the insert function and perform other linked list operations as needed.
 
Program:

    struct Node{ char data;
    struct Node *next;
    }*head;
    
    void insert(char data)
    {
    struct Node *n=(struct Node*)malloc(sizeof(struct Node)); struct Node *temp;
    if(head==NULL)
    {
    head=n;
    n->data=data; n->next=NULL; temp=head; return;
    }
    while(temp->next!=NULL)
    {
    temp=temp->next;
    }
    n->data=data; n->next=NULL; temp->next=n;
    }

Output:

<img width="389" height="360" alt="437745694-be023e9f-aed3-4b19-a712-8485fce48346" src="https://github.com/user-attachments/assets/26c00132-deee-4877-9761-c71ecdc98978" />


 
Result:
Thus, the program to insert a node in a linked list is verified successfully.


 
EXP NO:18 C PROGRAM TO TRAVERSE A DOUBLY LINKED LIST
Aim:
To write a C program to traverse a doubly linked list.

Algorithm:
1.	Initialize a temporary pointer (temp) to the head of the list.
2.	Use a while loop to traverse the list until the end (temp == NULL) is reached.
3.	Inside the loop, print the data of the current node.
4.	Move to the next node by updating the temp pointer to point to the next node (temp = temp->next).
 
Program:
     struct Node
     {
     struct Node *prev; struct Node *next; int data;
     }*head;
     void display()
     {
     struct Node *temp; temp=head; while(temp!=0)
     {
     printf("%d ",temp->data); temp=temp->next;
     }



}

Output:

<img width="325" height="400" alt="437746011-d08d112f-e4ce-4b4f-aa2e-1eced8b65030" src="https://github.com/user-attachments/assets/5fad906c-2c6b-40f4-a008-6dca318e2dbc" />



Result:
Thus, the program to traverse a doubly linked list is verified successfully. 



EXP NO:19 C PROGRAM TO INSERT AN ELEMENT IN DOUBLY LINKED LIST
Aim:
To write a C program to insert an element in doubly linked list

Algorithm:
1.	Create a new node (newNode) and allocate memory for it.
2.	Set the data of the new node to the provided value.
3.	If the list is empty, set the new node as the head.
4.	If the list is not empty, traverse the list to find the last node.
5.	Set the new node's prev pointer to the last node and update the last node's next pointer to the new node.
 
Program:

     struct Node
     {
     struct Node *prev; struct Node *next; float data;
     }*head;
     void insert(float data)
     {
     
     struct Node *n=(struct Node*)malloc(sizeof(struct Node)); struct Node *temp;
     if(head==NULL)
     {
     head=n;
     n->data=data; n->next=NULL; n->prev=NULL; temp=head;
     }
     else
     {
     while(temp->next!=NULL)
     {
     temp=temp->next;
     }
     n->data=data; n->next=NULL; n->prev=temp; temp->next=n;
     }
     
     
     }

Output:

<img width="403" height="540" alt="437746249-112a2d91-2a77-4940-93c1-dee038961f30" src="https://github.com/user-attachments/assets/70d66dfe-6b69-4deb-8f82-50e641c8aa33" />


Result:
Thus, the program to insert an element in doubly linked list is verified successfully.




EXP NO:20 C FUNCTION TO DELETE A GIVEN ELEMENT IN THE GIVEN LINKED LIST




Aim:
To write a C function that deletes a given element from a linked list.

Algorithm:
1.	Check if the Linked List is Empty:
o	If the head of the linked list is NULL, print a message indicating the list is empty and exit the function.
2.	Traverse the Linked List:
o	Start from the head node and iterate through the list to find the node that contains the given element (data).
3.	Handle Deletion of the First Node:
o	If the element to be deleted is found in the head node:
	Update the head of the linked list to point to the next node (i.e., head = head->next).
	Free the memory allocated to the node to be deleted.
	Exit the function.
4.	Traverse and Delete from the Middle or End:
o	If the element is not in the head node, continue traversing the list by checking each node’s next pointer.
o	When the node with the element is found, update the previous node’s next pointer to point to the next node of the node to be deleted (prev->next = current->next).
o	Free the memory allocated to the node to be deleted.
5.	Handle the Case when the Element is Not Found:
o	If the element is not found in any node, print a message indicating the element is not present in the list.
6.	End the Function.


Program:

     struct Node{
         char data; 
         struct Node *next;
     }*head;
     void delete()
     {
         if(head==NULL){
             printf("List is empty\n");
             return;
         }
         else if(head->next==NULL){
             head=NULL;
             free(head);
             printf("Node deleted from the begining ...\n");
         }
         else{
             struct Node *ptr;
             ptr=head;
             head=head->next;
             free(ptr);
             printf("Node deleted from the begining ...\n");
         }
     }

Output:


<img width="916" height="570" alt="437746315-1ac9a13d-2840-42ee-8beb-8605f3d67c25" src="https://github.com/user-attachments/assets/b2a0f358-86df-4514-894d-b332e83a81b5" />





Result:
Thus, the function that deletes a given element from a linked list is verified successfully.





