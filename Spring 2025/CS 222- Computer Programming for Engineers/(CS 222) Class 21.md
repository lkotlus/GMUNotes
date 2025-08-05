### Queues, Ordered Lists, BSTs
- Nothing new under the sun.
- Ordered lists are just sorted linked lists. They're $O(n)$ insert.
- BSTs are sick. Larger elements to the right, smaller elements to the left.
- We can do a little preprocessor directive trick to make using `malloc` a bit easier:

```c
#define TYPED_ALLOC(type) (type*)malloc(sizeof(type))

// These two definitions are logically equivalent:
node_t* n1 = (node_t*)malloc(sizeof(node_t));
node_t* n1 = TYPED_ALLOC(node_t);
```