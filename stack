#include <stdio.h>
#include <ctype.h>  

int top = -1, stack[100];

void push(int n);
int pop();
int eval(char ch, int op1, int op2);

void main() {
    char a[50], ch;
    int i, op1, op2, res, x;

    
    printf("Enter a postfix expression: ");
    fgets(a, sizeof(a), stdin);

    for (i = 0; a[i] != '\0'; i++) {
        ch = a[i];

        if (isdigit(ch)) { 
            push(ch - '0'); 
        }
        else if (ch != ' ' && ch != '\n') { 
            op2 = pop();
            op1 = pop();
            res = eval(ch, op1, op2);
            push(res);
        }
    }

    x = pop();
    printf("Evaluated value = %d\n", x);
}

void push(int n) {
    top++;
    stack[top] = n;
}

int pop() {
    int res = stack[top];
    top--;
    return res;
}

int eval(char ch, int op1, int op2) {
    switch (ch) {
        case '+': return (op1 + op2);
        case '-': return (op1 - op2);
        case '*': return (op1 * op2);
        case '/': return (op1 / op2);
        default: return 0; 
    }
}
