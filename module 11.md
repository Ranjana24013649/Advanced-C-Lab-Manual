

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

     int max_of_four(int a,int b,int c,int d){
         if(a>b&&a>c&&a>d){
             return a;
         }
         else if(b>a&&b>c&&b>d){
             return b;
         }
         else if(c>a&&c>b&&c>d){
             return c;
         }
         else{
             return d;
         }
     }
     int main(){
         int a,b,c,d;
         scanf("%d%d%d%d",&a,&b,&c,&d);
         printf("%d",max_of_four(a,b,c,d));
         return 0;
     }

Output:

<img width="868" height="314" alt="500791609-ec5ffc83-7e96-44ab-85a8-2ca8978a3e50" src="https://github.com/user-attachments/assets/ac56edb6-49ef-497a-a94a-3e8dfdd232c8" />


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

     #include <string.h>
     #include <math.h>
     #include <stdlib.h>
     void calculate_the_maximum(int n, int k) {
      int max_and = 0, max_or = 0, max_xor = 0;
         for (int i = 1; i <= n; i++) {
             for (int j = i + 1; j <= n; j++) {
                 int temp_and = i & j;
                 int temp_or = i | j;
                 int temp_xor = i ^ j;
                 if (temp_and > max_and && temp_and < k) {
                     max_and = temp_and;
                 }
                 if (temp_or > max_or && temp_or < k) {
                     max_or = temp_or;
                 }
                 if (temp_xor > max_xor && temp_xor < k) {
                     max_xor = temp_xor;
                 }
             }
         }
         printf("%d\n%d\n%d", max_and, max_or, max_xor);
     
     }
     
     int main() {
         int n, k;
       
         scanf("%d %d", &n, &k);
         calculate_the_maximum(n, k);
      
         return 0;
     }
     

Output:

<img width="868" height="314" alt="500791609-ec5ffc83-7e96-44ab-85a8-2ca8978a3e50" src="https://github.com/user-attachments/assets/70684d65-192b-418a-b933-853422b93015" />



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
     #include <string.h>
     #include <math.h>
     #include <stdlib.h>
     void calculate_the_maximum(int n, int k) {
      int max_and = 0, max_or = 0, max_xor = 0;
         for (int i = 1; i <= n; i++) {
             for (int j = i + 1; j <= n; j++) {
                 int temp_and = i & j;
                 int temp_or = i | j;
                 int temp_xor = i ^ j;
                 if (temp_and > max_and && temp_and < k) {
                     max_and = temp_and;
                 }
                 if (temp_or > max_or && temp_or < k) {
                     max_or = temp_or;
                 }
                 if (temp_xor > max_xor && temp_xor < k) {
                     max_xor = temp_xor;
                 }
             }
         }
         printf("%d\n%d\n%d", max_and, max_or, max_xor);
     
     }
     
     int main() {
         int n, k;
             scanf("%d %d", &n, &k);
         calculate_the_maximum(n, k);
       
     return 0;
     }
 
    

Output:

<img width="696" height="222" alt="500793117-c35eb95b-390d-4e29-8f5c-4ad54f5e7162" src="https://github.com/user-attachments/assets/1d496634-6caf-4397-a9d9-2a560252566c" />



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

     #include<stdlib.h>
     int main(){
         int *a,s,sum=0;
         scanf("%d",&s);
         a=(int *)malloc(sizeof(int)*s);
         for(int i=0;i<=s;i++){
             scanf("%d",&a[i]);
             sum+=a[i];
         }
         printf("%d",sum);
     }

Output:



<img width="634" height="219" alt="500795577-255f62a2-133b-4956-a5ec-6cbf08912fa9" src="https://github.com/user-attachments/assets/16efc7a3-bee1-4213-8f1a-efb96c20f8e6" />

 


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

     int countWords(char sentence[]) {
         int count = 1; 
         for (int i = 0; sentence[i] != '\0'; ++i) {
            printf("%c",sentence[i]);
             if (sentence[i] == ' ') {
                 count++;
                  printf("\n");
             }
                  }
     
         return count;
     }
     
     int main() {
         char sentence[1000];
         fgets(sentence,sizeof(sentence),stdin);
         printf("\nNumber of words: %d\n", countWords(sentence));
     
         return 0;
     }
     
OUTPUT:


<img width="622" height="559" alt="500796665-44158562-608e-4db5-b5a2-59d284db637f" src="https://github.com/user-attachments/assets/80ed2ac5-4f91-48ed-acde-5dc157302879" />







Result:

Thus, the program that counts the number of words in a given sentence is verified 
successfully.
