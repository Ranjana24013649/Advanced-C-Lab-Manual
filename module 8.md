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

    #include<stdio.h> #include<math.h> int main()
    {
    int n; scanf("%d",&n);
    if(n>=1 && n<=pow(4,3))
    {
    switch(n)
    {
    case 5:
    {
    printf("seventy one"); break;
    }
    case 6:
    {
    printf("seventy two"); break;
    }
    case 13:
    {
    printf("seventy three"); break;
    }
    case 14:
    {#include<stdio.h> #include<math.h> int main()
    {
    int n; scanf("%d",&n);
    if(n>=1 && n<=pow(4,3))
    {
    switch(n)
    {
    case 5:
    {
    printf("seventy one"); break;
    }
    case 6:
    {
    printf("seventy two"); break;
    }
    case 13:
    {
    printf("seventy three"); break;
    }
    case 14:
    {
    Printf("seventy nine"); break;
    }
    default:
    {
    printf("Greater than 13");
    }
    }
    }
    }




Output:


<img width="479" height="231" alt="437741451-34294cd8-ae6b-47c1-82de-90015920422a" src="https://github.com/user-attachments/assets/cb07e309-bd99-478a-8a38-47f794184369" />







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

   {
   char a[50]; scanf("%s",a); int l=strlen(a); char h='0';
   for(int i=0;i<4;i++)
   {
   int c=0;
   for(int j=0;j<l;j++)
   {
   if(a[j]==h)
   {
   c+=1;
   }
   }
   printf("%d ",c); h++;
   }
   }
   



Output:


<img width="652" height="216" alt="437741711-3d355b22-882d-4614-9473-8127a8d66ad5" src="https://github.com/user-attachments/assets/a932f65e-fdb3-49e6-b60b-5a69c0cfcdc6" />







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

    #include<stdio.h> #include<string.h> #include<stdlib.h>
    int next_per(int n, char **s)
    {
    for(int i = n - 1 ; i > 0 ; i--) if(strcmp(s[i],s[i-1]) > 0)
    {
    int j=i+1;
    for(;j<n;j++) if (strcmp(s[j],s[i-1])<=0) break; char *t=s[i-1];
    s[i-1]=s[j-1];
    s[j-1]=t;
    for(;i<n-1;i++,n--)
    {
    t=s[i]; s[i]=s[n-1]; s[n-1]=t;
    }
    return 1;
    }
    for(int i=0;i<n-1;i++,n--)
    {
    char *t=s[i]; s[i]=s[n-1]; s[n-1]=t;
    }
    return 0;
    }
    int main()
    {
    char **s; int n;
    scanf("%d",&n); s=calloc(n,sizeof(char*)); for(int i=0;i<n;i++)
    {
    s[i]=calloc(n,sizeof(char*)*5); scanf("%s",s[i]);
    }
    do
    {
    for(int i=0;i<n;i++) printf("%s%c",s[i],i==n-1?'\n':' ');
    }
    while(next_per(n,s));
     
    {
    for(int i=0;i<n;i++) free (s[i]);
    free(s); return 0;
    }
    }




Output:

<img width="344" height="393" alt="437742066-94ac185a-4a49-4e6d-9e76-2076873261cf" src="https://github.com/user-attachments/assets/e6a237fe-8a25-4709-9b7c-5be6a1be4c4f" />






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

   {
   int n,i,j,min; scanf("%d",&n);
   int len=n*2-1; for (i=0;i<len;i++)
   {
   for (j=0;j<len;j++)
   {
   min=i<j?i:j;
   min=min<len-i-1?min:len-1-i; min=min<len-j-1?min:len-1-j; printf("%d ",n-min);
   }
   printf("\n");
   }
   return 0;
   }




Output:

<img width="447" height="482" alt="437742210-9cd8fe3d-2946-4b2f-b203-6ab985687a05" src="https://github.com/user-attachments/assets/a3aeb4b2-6b58-4e78-a2a8-ad324a5e5082" />







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

  #include <stdio.h>
  void square();
  int main(){
      
      square();
      return 0;
  }
  void square(){
      int a;
      scanf("%d",&a);
      float ans = a*a;
      printf("The square of %d is : %.2f",a,ans);
  }




Output:

<img width="877" height="250" alt="437742412-b59c95d7-882c-4f93-aefc-786595eb3306" src="https://github.com/user-attachments/assets/c6722637-22b1-479b-9fe6-259db82ae1ad" />






Result:
Thus, the program is verified successfully



























