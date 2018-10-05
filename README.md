#include<stdio.h>
int top=-1,stack[5],item,i;
void push(int);
int pop();
void display();
void main()
{
    while(1)
    {
    int choise;
    printf("enter your choise\n");
    printf("push-1\npop-2\ndisplay-3\n");
    scanf("%d",&choise);
    
    switch(choise)
    {
        case 1:scanf("%d",&item);
                push(item); break;
        case 2:pop(); break;
        case 3:display() ; break;
        case 4:printf("exit point");break;
    }
        
    }
}
 void push(int item)
{
    printf("%d",top);
    if(top==4)
    { 
        printf("overflow codition");
            }
    else
    {
        top++;
        
        stack[top]=item;
    }
}
int pop()
{
 if(top=-1)
 {
     printf("underflow condition");
 }
 else
 {
    printf("deleted element%d",stack[top]);
    top--;
     
 }
}
void display()
{
    if(top==-1)
 {
     printf("underflow condition");
 }
 else
 {
     for (i=0;i<5;i++)
     {
         printf("%d\n",stack[i]);
     }
 }
}
