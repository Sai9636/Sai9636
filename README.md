#include <stdio.h> 
#include <stdlib.h>
 char stk[10]; 
int top=-1; 
void push(char ch) 
{top++;
 stk[top]=ch; 
} 
void pop(char ch)
 {if(((stk[top]=='(')&&(ch==')'))||((stk[top]=='{')&&(ch=='}')||(stk[top]=='[')&&(ch==']'))) top--; } 
int main() 
{char ch[10];
 printf("enter the exp :");
 gets(ch); 
for(int i=0;ch[i]!='\0';i++) 
{if((ch[i]=='{')||(ch[i]=='[')||(ch[i]=='(')) 
   push(ch[i]);
 else if((stk[i]=='}')||(stk[i]==']')||(stk[i]==')'))                       pop(stk[i])
 } 
if(top==-1)
   printf("brackets check sucessful");
else 
    printf("unsucessful");
 return 0; }
