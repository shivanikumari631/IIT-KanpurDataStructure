# Compilation process of a program:
- Commands can be used in powershell or cmd to step by step compilation:

		1. gcc -E program.c -o program.i //Expandable Code
		2. gcc -S program.i -o program.s //Assembly Code
		3. gcc -E program.s -o program.o //Object Code
		4. gcc -v program.o -o program.exe //Executable Code

![image](https://drive.google.com/uc?export=view&id=1d8xK2HFH99DNw31xhIW5vZyvfv0MGxFh)

# Functions:

- Set of statement or block of code that perform some tasks.

- Functions can be use multiple times depend on function call.

- The idea is to use some commonly or repeatedly done task together and make a function so that instead of writing the same code again and again we can call that function.

- Types of Functions:

		1. System Defined/Predefined/library Function/built-in Function (printf, scanf, etc).
		2. User Defined Function => Used to customize user's task.

### How create user defined function?

#### Function Declaration

- <strong> Syntax </strong>: return_type function_name(argument);
- <strong> ReturnType </strong>: void (no return), int, char, float etc.
- <strong> FunctionName </strong>: Valid Identifier
- <strong> Argument </strong>: What you want to pass to the function.

#### Function Definition:
	```
	Syntax: return_type function_name(argument) {
	------
	------
	}
	```

Function Calling:

	FunctionName(argument);

1. A variable name can begin only with an underscore or an alphabet (any case).
2. It can thereafter consist of any number of _(underscore), alphabets and numbers.
3. No special characters other than _ is allowed.

# 15 SEPT 2020:

	1. getch()

		 => To take input, user cannot see, on the spot assigning
		 => No need to press enter.
		 => No argument with return.

	2. getche()

		 => To take input, user can see, on the spot assigning.
		 => No need to press enter.

	3. getchar()

		 => To take input, user can see, for assigning pressing enter button is needed.

# Array:
- An Array is a collection of similar data items and these data items may be all int, float or all char.
- Each member of an array is identified by unique index or subscript assigned to it.
- An Array is defined in the same way as a variable is defined except that, the array name is followed by one or more expressions, enclosed withing square brackets[], specifying the array dimension.
- The general Syntax of an array is:

SYNTAX: data_type ArrayName[SIZE];

	Array Disadvantage:
	-> Similar datatype storage ==> Disadvantage. => overcome structure
	-> Size cannot be modified.
	-> Memory waste

Dynamic Memory Allocation functions: => Run-time Memory Allocation.

	1. malloc()
	2. calloc()
	3. realloc()
	4. free()

# Pointer:

- Pointer is special variable that holds the address of any memory (address).
- To create pointer variable, variable should start with * symbol.

##### Syntax: datatype *pointerVariable;

	```
	for e.g,
			#include<stdio.h>
			void main(){
				int a; //variable
				a = 10;
				printf("%d\n", a);
				printf("%u\n", &a);
			}
	```

# Structure:

##### Structure Syntax:

	```
	struct structureName{
		-------
		-------
	}structureVariable;
	or
	struct structureName{
		-------
		-------
	};
	struct structureName structureVariable;
	```

<strong>Accessing member: </strong> structureVariable.MemberName //period operator


	```
	struct structureName{
		-------
		-------
	}*structureVariable; //ptr_to_struct
	or
	struct structureName{
		-------
		-------
	};
	struct structureName *structureVariable;
	```

<strong>Accessing member: </strong>  structureVariable->MemberName //Arrow operator

# Array to pointer:

		```
		for e.g,
		#include<stdio.h>
		void main(){
			int a = 11, b=22, c=33,d=44, e=55; //variable
			int *ptr[5];
			ptr[0] = &a;
			ptr[1] = &b;
			ptr[2] = &c;
			ptr[3] = &d;
			ptr[4] = &e;
			for(int i = 0; i<5 ; i++){
				printf("%u => %d\n", ptr[i], *ptr[i]);
			}
		}
		```

# Data Structure:

- Data Structure is a representation of logical relationship existing between individual elements of data.
- In other words, a data structure defines a way of organizing all data items that considers not only the elements stored	but also their relationship to each other.
- The term data structure is used to describe the way data is stored.
- To develop a program of an algorithm, we should select an appropriate data structure for that algorithm. Therefore, data structure is represented as:

		Algorithm + Data Structure = Program

# Algorithm:

An algorithm is a finite sequence of instructions, each of which has a clear meaning and can be performed with a finite amount of effort in a finite length of time. No matter what the input values may be, an algorithm terminates after executing a finite number of instructions. In addition, every algorithm must satisfy the following criteria:

	1. Input: there are zero or more quantities, which are externally supplied;

	2. Output: at least one quantity is produced;

	3. Definiteness: each instruction must be clear and unambiguous;

	4. Finiteness: if we trace out the instructions of an algorithm, then for all cases the
	algorithm will terminate after a finite number of steps;

	5. Effectiveness: every instruction must be sufficiently basic that it can in principle be
	carried out by a person using only pencil and paper. It is not enough that each operation
	be definite, but it must also be feasible.

# Introduction:
- Memory can be understand as a piece of area which a program needs to run it self.

- A computer program always needs some amount of memory to run which is allocated to it by Operating System.

		To run any process, an O.S. allocates it, separate memory.

- A program requests the amount of memory which it needs to run itself from O.S. Then OS Manages this memory.

- Memory can be allocated in following:
		1. Static memory allocation
		2. Dynamic memory allocation

# Different Part Of Program Memory:
- It is the area which is used to store all source code like .c Or .cpp files.

- <strong> Stack: </strong>
It is the area which is used to store variables like
int a, char name[20], float height

- <strong> Heap: </strong>
It is the area which operating system allocates us when we
request it at run time of a program.


	```
	int *ptr; //pointer to integer
	char *a; //pointer to character
	void *n; // void pointer or generic pointer
	```

# Type casting: converting from one type to another type.
Types of type casting:
1. Implicit(automatic)

		for e.g,
			#. float n = 5.67;
			#. int a = 2.5;
			#. char ch ='a';
			#. ch = ch + 32;
			#. int n = 56;
			#. char ch;
			#. ch = n + n;

2. Explicit(Manually)

		Syntax: (data_type)Varible;

# Dynamic Memory in C:
- Function Which Can Be Used For Dynamic Memory Allocation Are :-

		Void * malloc(int)
		1.It allocates specified number of bytes from the heap and return a void
		type of pointer pointing towards the base address of that address.

		return_type void_pointer;

		2. Void * calloc(int,int)
		It also allocates specified number of bytes from heap but the difference is that memory is shattered.

		return_type void_pointer;

		3. Void * realloc(void *,int size)
		It reallocates a free memory to us.

		4. Void free(void *)
		It deallocates the memory from the heap which is previously allocated.

			```
			int a=10;
			int* ptr = &a;
			scanf("%d", &a); or scanf("%d", ptr);
			```

# Pointer Increment & Scale Factor:
- Pointer increment means its value is increased by the length of the data type that it points to, and this length is called as scale Factor.

		for e.g, int *ptr;
			   ptr = ptr + 1;
			   ptr = 0x2012 + 4;

- Sizeof(var_name) function is used to know the no of bytes need for that variable.

# Operations with pointers:

Addition and subtraction are the only arithmetic operations that can be performed on pointers.

	For e.g,
		p1= p1 + 4;
		p1 = p1 - 2;
		p3 = p1 - p2;

	Following operations are valid with pointers:
		if(p1 > p2){
			------
		}

		if(p1 != p2){
			------
		}

		if(p1 == p2){
			------
		}

		p1++;

		--p2;

		sum += *p2;

# Data Structure:
![image](https://drive.google.com/uc?export=view&id=1ITXoDo-VtJ9W_toIAqrjXPcMIDHdbido)

# Linked List:

- Linked Lists and arrays are similar since they both store collection of data.

- Array is the most common data structure used to store collection of elements.

- Arrays are convenient to declare and provide the easy Syntax to access any element by its index number. Once the array is set up, access to any element is convenient and fast.

- A linked list data structure include a series of connected nodes. Here, each node and the address of the next node:

		1. A data item
		2. An address of another nodes
		3. We wrap both the data item and the next node reference in a struct.
	

# Representation of Linked List:

	```
	struct node{
		int data;
		struct node *next;
	}
	```

Each struct node has a data item and a pointer to another struct node.
Let us create a simple Linked List with three items to understand how this works.

		//Initialize nodes
		struct node * head;
		struct node * one = NULL;
		struct node *two = NULL;
		struct node * three = NULL;

		//Allocate memory
		one = malloc(sizeof(struct node));
		two = malloc(sizeof(struct node));
		three = malloc(sizeof(struct node));

		//Assign data values
		one->data = 1;
		two->data = 2;
		three->data=3;

		//Assign data values
		one->data = 1;
		two->data = 2;
		three->data=3;

		//Connect nodes
		one->next = two;
		two->next = three;
		three->next = NULL;

		//Save address of first node in head
		head = one;

# Singly Linked List:

- It is the most common. Each node has data and a pointer to the next node.

# Circular Linked List:

- A Circular linked list is variation of a linked list in which the last element is linked to the first element.
This forms a circular loop.

# Doubly Linked List:

- We add a pointer to the previous node in a Doubly-linked list. Thus, we can go in either direction: Forward or Backward.

# Circular Doubly Linked List:

- We add a pointer to the previous node in a Doubly-linked list. Thus, we can go in either direction: Forward or Backward.

	NOTE: The power of Linked List comes from the ability to break the chain and rejoin it.

# Operations on linked list:

	1. Creation
	2. Traversing
	3. Searching
	4. Insertion
	5. Deletion
	6. Updation

# Inserting a node in the begining:

Algorithm to be followed to insert a new node at the beginning of the list:

- Allocate new memory block
- If the list is empty then start = newnode.
- If the list is not empty, follow the steps given below:

		```
		newnode -> next = start;
		start = newnode;
		```

# Inserting a node at the end:

Algorithm to insert a new node at the end of the list:

- Allocate new memory block.
- If the list is empty then start = newnode
- If the list is not empty follow the steps given below:
		
		```
		temp = start;
		while(temp->next != NULL){
			temp = temp->next;
		}
		temp->next = newnode;

		```

# Inserting a node at intermediate (Specific) Position:

Algorithm to insert a new node in an intermediate position in the list:

- Allocate new memory block
- Ensure that the specified position is in between first node and last node. If not, specified position is invalid.
- Store the starting address (which is in start pointer) in temp and prev pointers.
- Then traverse the temp pointer upto the specified position followed by prev pointer.
- After reaching the specified position, follow the steps given below:

		```
		prev -> next = newnode;
		newnode -> next = temp;
		```

# Linked List Applications:

	1. Dynamic Memory Allocation.
	2. Implemented in stack and queue.
	3. In undo functionality of software
	4. Hash tables, Graphs

# STACK:

1. A stack is a list of elements in which an element may be inserted or deleted only at one end, called the top of the stack. Stacks are sometimes known as LIFO(Last in, first out) lists.

2. As the items can be added or removed only from the top i.e, the last item to be added to a stack is the first item to be removed.

3. The two basic operations associated with stacks are:

		1. Push: Is the term used to insert an element into a stack.

![image](https://drive.google.com/uc?export=view&id=1bse0K_BUSvh3XpB3t9NNSwLJKNGq7OFt)

		2. Pop: Is the term used to delete an element from a stack.

![image](https://drive.google.com/uc?export=view&id=1tOZLI3UjpWj0WGz2wg89EPKOULypt4fC)

4. Operations on Stacks:

	- Creation
	- Traversing
	- Searching
	- Insertion
	- Deletion
	- Updation

# Representation of STACK:

		1. Array Implementation of Stack(Static Implementation)

![image](https://drive.google.com/uc?export=view&id=1OkToZvW0PEv-e_gbPnML_TTCc5j7NncO)

		2. Linked List Implementation of Stack(Dynamic Implementation)

![image](https://drive.google.com/uc?export=view&id=1LClIceVMNGbLwMuJAmO0IsDTB_H9Kzfv)

# Applications of STACK:

	a. Stack Frame (Memory Structure)
	b. Reversing a String
	c. Calculation of Expressions

# Stack Frame / Memory Layout:

![image](https://drive.google.com/uc?export=view&id=1IhpZkOZ-4d8mziDXa1rgxNFdBplECMn5)

# Algebraic Expressions:

	1. An Algebraic expressions is a legal combination of operators and operands.
	2. Operand is the quantity on which a mathematical operation is performed.
		Operand may be a variable like x, y, z or a constant like 5, 4, 6 etc.
	3. Operator is a symbol which signifies a mathematical or logical operation between the operands.
		Examples of familiar operators include +, -, *, /, ^ etc.
	4. An Algebraic expression can be represented using three notations.
		They are infix, postfix and prefix notations.

# Infix:
It is the form of an arithmetic expression in which we fix (place) the
arithmetic operator in between the two operands.

		Example: A+B
		(A + B) * (C - D)

- Prefix: It is the form of an arithmetic notation in which we fix (place) the arithmetic operator before (pre) its two operands. The prefix notation is called as polish notation.

		Example: +AB
		*+AB - CD

- Postfix: It is the form of an arithmetic expression in which we fix (place) the arithmetic operator after (post) its two operands. The postfix notation is called as suffix notation and is also referred to reverse polish notation.

		Example: AB+
		AB + CD -*

# Five Binary Operations: +, -, *, /, ^(exponentiation)
For these binary operations, the following in the order of precedence (highest to lowest):

| Operator    				| Precedence   		|
| :----------: 				| :-----------: 	|
| exponentiation(^)   		| Highest    		|
| *, /   					| Next Highest 		|
| +, - 						|Lowest				|

# Convert Infix notation to prefix:

		1. If a infix expression is given so first check precedence of
		operators and make brackets according to that.

		This means higher precedence operator bracket first.

		2. We need to traverse whole expression and find opening
		brackets if finds fetch operator that combined in between
		them and if any operand will encountered then this will write in same sequence.

		3. If any operator or closing bracket is encountered so ignore
		that.

				for e.g. A+B*C
						=> A+(B*C)
						=> (A+(B*C))
						=> +A*BC

				for e.g. A*B+CAD
						=> A*B+(CAD)
						=> (A*B)+(CAD)
						=> ((A*B)+(C^D))
						=> +*AB^CD


				for e.g. A^B*C-D/E
						=> (A^B) *C-D/E
						=> ((A^B) *C)-D/E

				for e.g. ((A^B) *C)-(D/E)
						=> (((A^B) *C)-(D/E))
						=> -*^ABC/DE


# Convert Infix notation to postfix:
1. If a infix expression is given so first check precedence of operators and make brackets according to that. This means higher precedence operator bracket first.

2. we need to traverse whole expression and find closing brackets if finds fetch operator that combined in between them and if any operand will encountered then this will write in same sequence.

3. If any operator or opening bracket is encountered so ignore that.

				for e.g. A+B*C
						=> A+(B*C)
						=> (A+(B*C))
						=> ABC*+

				for e.g. A+B*C/D
						=> A+(B*C) /D
						=> A+((B*C) /D)
						=> (A+((B*C) /D))
						=> ABC*D/+

				for e.g. (A + B) * (C - D) / E
						=> ((A+B) *(C-D)) /E
						=> (((A+B) *(C-D)) /E)
						=> Postfix: AB+CD-*E/
						=> Prefix: *+AB-CDE

# Queue:
- A queue is another special kind of list, where items are inserted at one end called the rear and deleted at the other end called the front. Another name for a queue is a "FIFO" or "First-in-first-out" list.

- The operations for a queue are analogues to those for a stack, the difference is that the insertions go at the end of the list, rather than the beginning. We shall use the following operations on queues:

		1. enqueue: which inserts an element at the end of the queue.

		2. dequeue: which deletes an element at the start of the queue.

# Representation of Queue:

![image](https://drive.google.com/uc?export=view&id=1-sR8kTbwR2HwxTfv9ozZHpVwOVE4WOZk)

# Queue Implementation:

	1. Using Array
	2. Using Linked List

# Searching:

1. Refers to the operation of finding the location of a given item in a collection of items.
2. Searching is a technique of finding an element from the given data list or set of the elements like an array, list or trees.
3. It is a technique to find out an element in a sorted or unsorted list.
3. Types of Searching:

		1. Linear (Sequential) Search
		2. Binary Search

# Sorting:

Refers to the operation of arranging data in some given order, such as increasing or decreasing, with numerical data, or alphabetically, with character data.

## Bubble Sort Algorithm:

- Starting from the first index, compare the first and the second elements. If the first element is greater than the second element, they are swapped.
- Now, compare the second and the third elements. Swap them if they are not in order. The above program goes on until the last element.
- The same process goes on for the remaining iterations. After each iteration, the largest element among the unsorted elements is placed at the end.
- In each iteration, the comparison takes place up to the last unsorted element.
- The array is sorted when all the unsorted elements are placed at their correct positions.

# Tree:

- A tree is a non-linear hierarchical data structure taht consists of nodes connected by edges.
<!-- Image -->
## Tree Terminologies:
#### Node:
- A node is an entity that contains a key or value and pointers
to its child nodes.
- The last nodes of each path are called leaf nodes or external nodes that do not contain a link/pointer to child nodes.
- The node having at least a child node is called an internal
node.

#### Edge:
- It is the link between any two nodes.

<!-- Image -->
#### Leaf node:
- A node with no children is called a leaf (or external node).
A node which is not a leaf is called an internal node.

#### Path:
- A sequence of consecutive edges from the source node to
destination node.

- A sequence of nodes n1, n2, . . .,nk such that ni is the parent of ni + 1 for i = 1, 2,. . ., k - 1. The length of a path is 1 less than the number of nodes on the path. Thus there is a path of length zero from a node to itself.
For the tree shown in above figure, the path between A and I is A, B, D, I.

#### Siblings
- The children of the same parent are called siblings. 
- For the tree shown in figure, F & G are the siblings of the parent node C and H and I are the siblings of the parent node D.
#### Ancestor and Descendent:
- If there is a path from node A to node B, then A is called an ancestor of B and 
- B is called a descendent of A.

#### Root:
- It is the topmost node of a tree.

#### Height of a Node:
- The height of a node is the number of edges from the node to the deepest leaf (i.e,he longest path fromt he node to a leaf node).
#### Depth of a Node:
- The depth of a node is the number of edges from the root to the node.