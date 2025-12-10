# DATA STRUCTURES & ALGORITHMS – COMPLETE FINAL NOTES (PTU SYLLABUS)

==================================================
MODULE 1: INTRODUCTION & SEARCHING
==================================================

## Data Structure
A data structure is a way of organizing and storing data so that it can be accessed and modified efficiently.

## Types of Data Structures
Primitive: int, float, char  
Non-Primitive: Array, Stack, Queue, Linked List, Tree, Graph  

## Algorithm
An algorithm is a finite set of well-defined steps to solve a problem.

## Characteristics of Algorithm
- Input
- Output
- Definiteness
- Finiteness
- Effectiveness

--------------------------------------------------
LINEAR SEARCH
--------------------------------------------------

Definition: Linear search checks each element one by one.

Pseudocode:
START  
for i = 0 to n-1  
  if A[i] == key  
    return i  
return -1  
END  

Time Complexity:
Best: O(1)  
Worst: O(n)  
Space: O(1)  

--------------------------------------------------
BINARY SEARCH (Sorted Array)
--------------------------------------------------

Pseudocode:
START  
low = 0  
high = n-1  
while low <= high  
  mid = (low + high)/2  
  if A[mid] == key  
    return mid  
  else if A[mid] < key  
    low = mid + 1  
  else  
    high = mid - 1  
return -1  
END  

Time Complexity:
Best: O(1)  
Worst: O(log n)  

==================================================
MODULE 2: STACK & QUEUE
==================================================

## Stack
Stack is a LIFO data structure.

Operations:
Push, Pop, Peek

Pseudocode (Array Stack):

PUSH(x):  
if top == size-1 → Overflow  
top = top + 1  
stack[top] = x  

POP():  
if top == -1 → Underflow  
return stack[top--]  

Applications:
- Expression evaluation
- Undo/Redo
- Function calls
- Backtracking

--------------------------------------------------
INFIX TO POSTFIX
--------------------------------------------------

Scan expression from left to right  
If operand → print  
If '(' → push  
If ')' → pop till '('  
If operator → pop higher priority operators  

--------------------------------------------------
POSTFIX EVALUATION
--------------------------------------------------

Scan expression  
If operand → push  
If operator → pop 2 operands → apply → push result  

--------------------------------------------------
QUEUE
--------------------------------------------------

Queue is FIFO data structure.

ENQUEUE(x):  
if rear == size-1 → Overflow  
rear++  
Q[rear] = x  

DEQUEUE():  
if front > rear → Underflow  
return Q[front++]  

Types:
- Simple Queue
- Circular Queue
- Priority Queue
- Deque

==================================================
MODULE 3: LINKED LIST & TREES
==================================================

--------------------------------------------------
SINGLY LINKED LIST
--------------------------------------------------

Insertion at Beginning:  
new->next = head  
head = new  

Deletion:  
Traverse → update links → free node  

--------------------------------------------------
DOUBLY LINKED LIST
--------------------------------------------------

Each node has:
prev | data | next  

--------------------------------------------------
CIRCULAR LINKED LIST
--------------------------------------------------

Last node points to head.

--------------------------------------------------
BINARY TREE TRAVERSALS
--------------------------------------------------

Inorder: Left → Root → Right  
Preorder: Root → Left → Right  
Postorder: Left → Right → Root  

--------------------------------------------------
BINARY SEARCH TREE (BST)
--------------------------------------------------

Insertion Rule:
Left < Root < Right  

Deletion:
- No child  
- One child  
- Two children (replace with inorder successor)

Complexity:
Best: O(log n)  
Worst: O(n)  

--------------------------------------------------
AVL TREE
--------------------------------------------------

Self-balancing BST.

Balance Factor = Height(left) - Height(right)

Rotations:
- LL
- RR
- LR
- RL

Always maintains O(log n)

--------------------------------------------------
B-TREE & B+ TREE
--------------------------------------------------

Used in Databases  
Multi-level indexing  
All leaf nodes at same level  
Operations in O(log n)

==================================================
MODULE 4: SORTING & HASHING
==================================================

--------------------------------------------------
SELECTION SORT
--------------------------------------------------

Pseudocode:
for i = 0 to n-2  
  min = i  
  for j = i+1 to n-1  
    if A[j] < A[min]  
      min = j  
  swap(A[i], A[min])

Comparisons = n(n-1)/2  
Time: Best = O(n²), Worst = O(n²)  
Space: O(1)  
Stable: No  

--------------------------------------------------
BUBBLE SORT
--------------------------------------------------

Pseudocode:
for i = 0 to n-1  
  for j = 0 to n-i-2  
    if A[j] > A[j+1]  
      swap  

Comparisons = n(n-1)/2  
Best = O(n)  
Worst = O(n²)  
Stable: Yes  

--------------------------------------------------
INSERTION SORT
--------------------------------------------------

Pseudocode:
for i = 1 to n-1  
  key = A[i]  
  j = i-1  
  while j>=0 and A[j] > key  
    A[j+1] = A[j]  
    j--  
  A[j+1] = key  

Best = O(n)  
Worst = O(n²)  
Stable: Yes  

--------------------------------------------------
MERGE SORT
--------------------------------------------------

Divide array → sort → merge  

Time: O(n log n)  
Space: O(n)  
Stable: Yes  

--------------------------------------------------
QUICK SORT
--------------------------------------------------

Pivot selection → partition → recursive sort  

Best: O(n log n)  
Worst: O(n²)  
Space: O(log n)  
Stable: No  

--------------------------------------------------
HEAP SORT
--------------------------------------------------

Build Max Heap → Swap → Heapify  

Time: O(n log n)  
Space: O(1)  
Stable: No  

--------------------------------------------------
HASHING
--------------------------------------------------

Maps key to index using hash function  
Used for fast search  
Collision handled using:
- Chaining
- Open Addressing

==================================================
MODULE 5: GRAPH
==================================================

Graph = Set of vertices + edges

Representations:
- Adjacency Matrix
- Adjacency List

--------------------------------------------------
BFS (Breadth First Search)
--------------------------------------------------

Uses Queue

START from source  
Visit neighbours  
Repeat  

Time: O(V+E)

--------------------------------------------------
DFS (Depth First Search)
--------------------------------------------------

Uses Stack / Recursion  

Visit node → go deep → backtrack  

Time: O(V+E)

==================================================
COURSE OUTCOMES SUMMARY
==================================================

- Analyze time & space complexity  
- Implement Stack, Queue, Linked List, Trees  
- Implement Sorting & Searching  
- Choose correct data structure for real-world problems  

==================================================
END OF FINAL NOTES
==================================================
