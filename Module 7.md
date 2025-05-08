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
```
#include<stdio.h>
#include<math.h> 
int main()
{
    int n; 
    scanf("%d",&n);
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
        printf("seventy four"); break;        
    }
    case 15:
    {
        printf("seventy five"); break;        
    }
    case 16:
    {
        printf("seventy six"); break;        
    }
    case 5:
    {
        printf("seventy seven"); break;        
    }
    case 6:
    {
        printf("seventy eight"); break;        
    }
    case 13:
    {
        printf("seventy nine"); break;        
    }
    default:
    {
        printf("Greater than 13");        
    }
}
}
}
```
Output:

![image](https://github.com/user-attachments/assets/f9a8056b-9ea3-4d92-ac2a-c49a496bfa26)



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
```
#include<stdio.h>
#include<string.h> 
int main()
{
    char a[50]; 
    scanf("%s",a); 
    int l=strlen(a); char h='0';
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
        printf("%d ",c); 
        h++;
    }
}
```
Output:

![image](https://github.com/user-attachments/assets/9272af7d-7a14-4b37-b665-2671a48128d6)

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
```
#include<stdio.h> 
#include<string.h> 
#include<stdlib.h>
int next_per(int n, char **s)
{
    for(int i = n - 1 ; i > 0 ; i--) 
    if(strcmp(s[i],s[i-1]) > 0)
    {
        int j=i+1;
        for(;j<n;j++) if (strcmp(s[j],s[i-1])<=0)
        break; char *t=s[i-1];
        s[i-1]=s[j-1];
        s[j-1]=t;
        for(;i<n-1;i++,n--)
        {
            t=s[i];
            s[i]=s[n-1];
            s[n-1]=t;  
        }
        return 1;   
    }
    for(int i=0;i<n-1;i++,n--)
    {
        char *t=s[i];
        s[i]=s[n-1]; 
        s[n-1]=t; 
    }
    return 0;   
}
int main()
{
    char **s; 
    int n;
    scanf("%d",&n);
    s=calloc(n,sizeof(char*)); 
    for(int i=0;i<n;i++)
    {
        s[i]=calloc(n,sizeof(char*)*5); 
        scanf("%s",s[i]);     
    }
    do
    {
        for(int i=0;i<n;i++) 
        printf("%s%c",s[i],i==n-1?'\n':' ');  
    }
    while(next_per(n,s));
    {
        for(int i=0;i<n;i++)
        free (s[i]);
        free(s);
        return 0;
    }
}
```
Output:

![image](https://github.com/user-attachments/assets/7e5a8feb-76e2-4251-a6ba-bf721547152b)

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
```
#include<stdio.h>
int main()
{
    int n,i,j,min;
    scanf("%d",&n);
    int len=n*2-1; for (i=0;i<len;i++)
    {
        for (j=0;j<len;j++)
        {
            min=i<j?i:j;
            min=min<len-i-1?min:len-1-i; 
            min=min<len-j-1?min:len-1-j; 
            printf("%d ",n-min);            
        }
        printf("\n");        
    }
    return 0;
}
```
Output:

![Screenshot 2025-05-08 135606](https://github.com/user-attachments/assets/c314c1f1-2ecc-4704-853d-c037794c983c)

Result:
Thus, the program is verified successfully



Ex No 5 : C PROGRAM TO DISPLAY STUDENT DETAILS USING STRUCTURE

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

10.Free the allocated memory

11.After all operations are done, call free(s) to release the dynamically allocated memory.

12.Return from the main function

13.End the program by returning 0.

Program:
```
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
```
Output:

![image](https://github.com/user-attachments/assets/2c5201a9-d13e-4902-97f9-d8299d32d87a)

Result:
Thus, the program is verified successfully
