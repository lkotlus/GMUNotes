### Linked Lists
- Yeah!
- We have a pointer to the next node. We also have a pointer to the previous node if it's a doubly linked list.
- That's the whole thing.
- Always free everything!
- We insert at the head!

### Stacks and Queues
- Typing the word "queue" feels like I just mash keys and hope for the best
- We implement these with LLs to be BLAZINGLY FAST
- Stacks just need a pointer for the top, whereas queues require a pointer for the front and back.
- Stacks use push and pop, queues use enqueue and dequeue.
- LIFO and FIFO
- Stack definition:

```c
typedef struct stack_node_t stack_node_t;
typedef struct stack_t stack_t;

struct stack_node_t {
	int val;
	stack_node_t* next;
}

struct stack_t {
	stack_node_t* top;
}
```

- Pop and push implementation:

```c
void push(stack_t *stack, int val) {
	stack_node_t *n = (stack_node_t*)malloc(sizeof(stack_node_t));
	n->val = val;
	n->next = stack->top;
	
	stack->top = n;
}

int pop(stack_t *stack) {
	// assumes that (stack->top != NULL)
	int returnval = stack->top->val;
	stack_node_t* old = stack->top;
	
	stack->top = stack->top->next;
	free(old);

	return returnval;
}
```

- Just a lil' pop and print:

```c
stack_t stack = {NULL};

push(&stack, 10);
push(&stack, 20);
push(&stack, 30);
push(&stack, 40);

while (stack.top != NULL) {
	printf("%d\n", pop(&stack));
}
```
