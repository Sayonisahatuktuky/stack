#include <stdio.h>
#include <stdlib.h>

#define STACK_MAX 100

typedef struct {
    int top;
    int data[STACK_MAX];
} stack;

void push(stack *s, int item);
int pop(stack *s); // Declare the pop function

void push(stack *s, int item) {
    if (s->top < STACK_MAX) {
        s->data[s->top] = item;
        s->top = s->top + 1;
    } else {
        printf("Stack is full\n");
    }
}

int pop(stack *s) {
    int item;
    if (s->top == 0) {
        printf("Stack is empty\n");
        return -1;
    } else {
        s->top = s->top - 1;
        item = s->data[s->top];
        return item; // Return the popped item
    }
}

int main() {
    stack my_stack;
    my_stack.top = 0;

    push(&my_stack, 1);
    push(&my_stack, 2);
    push(&my_stack, 3);



    int popped_item = pop(&my_stack); // Pop the top item
    if (popped_item != -1) {
        printf("Popped item: %d\n", popped_item);
    }

     for (int i = 0; i < my_stack.top; i++) {
        printf("Item %d: %d\n", i + 1, my_stack.data[i]);
    }
    return 0;
}
