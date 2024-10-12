# Experiment-17

## AIM
To study and implement stack implementation using array.

## Problem Statement
1.) Write a c++ program to do stack implementation.

# Theory
A stack is a data structure that operates on a Last In, First Out (LIFO) basis, where the last item added is the first one removed. You can push (add) and pop (remove) items from the top, with operations to check the top item and whether the stack is empty. Stacks can be implemented using arrays or linked lists and are commonly used in applications like undo mechanisms in text editors and managing function calls, offering flexibility through dynamic memory allocation.

## Program Codes
1)
```javascript
 //Sharvari Murade
//23070123088
#include <iostream>
using namespace std;
#define size 5
#define ERROR -9999
class Stack{
    int top, ar[size];
    public:
    Stack()
    {
        top=-1;
        ar[0]=0;
    }
    void push(int);
    int pop();
    int peak();
    void disp();
};
void Stack::push(int num)
{
    if (top==size-1)
    {
        cout<<"STACK OVERFLOW: Stack is full"<<endl;
        return;
    }
    else
    {
        ar[++top]=num;
    }
}
int Stack::pop()
{
    int val;
    if(top==-1)
    {
        cout<<"STACK UNDERFLOW: STACK IS EMPTY"<<endl;
        return ERROR;
    }
    else{
         val=ar[top--];
         return val;
    }
}
int Stack::peak()
{
    if(top==-1)
    {
        cout<<"STACK UNDERFLOW: stack is empty"<<endl;
        return ERROR;
    }
    else
    {
        return ar[top];
    }
}
void Stack::disp()
{
    if(top==-1)
    {
       cout<<"STACK UNDERFLOW: stack is empty"<<endl;
        return ;
    }
    else
    {
        int i=0;
        while(i!=(top+1))
        {
            cout<<ar[i]<<"  ";
            i++;
        }
    }
}
int main()
{
    Stack s1;
    s1.push(7);
    s1.push(10);
    s1.push(4);
    int val=s1.pop();
    cout<<val;
    int top=s1.peak();
    cout<<top;
    s1.disp();
    return 0;
}
```
## Program Output

<img width="297" alt="image" src="https://github.com/user-attachments/assets/e5347a4a-9962-42be-8b04-5131e14dd546">

## Conclusion
In summary, stacks are essential data structures that efficiently manage data in a specific order, making them invaluable for various programming tasks and applications that require organized and predictable data handling.

