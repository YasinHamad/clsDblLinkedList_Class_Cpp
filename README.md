# Brief Description
This class help you deal with doubly linked list with 16 different functionalities.

# Purpose
The purpose of this project is mainly to practice OOP and DSA.
The project is related to [ProgrammingAdvices Roadmap](https://programmingadvices.com/p/roadmap) - Course 13 - Project Number 01.
Feel free to check my notes/projects about this course [Course 13](https://github.com/YasinHamad/Programming_Basics/tree/main/course_13), and other courses [Programming Basics](https://github.com/YasinHamad/Programming_Basics).

# Functions
This is how you create an instance
```cpp
clsDblLinkedList<int> my_list; // or
clsDblLinkedList<string> my_list; // or
clsDblLinkedList<float> my_list; // you can choose the type you want
```

## Function number 01
`void InsertAtBeginning(element_type data)`  
Inserts the item at the beginning, it takes `O(1)`  
```cpp
clsDblLinkedList<int> my_list;
my_list.InsertAtBeginning(10);
my_list.InsertAtBeginning(20);
my_list.InsertAtBeginning(30);
my_list.InsertAtBeginning(40);
my_list.InsertAtBeginning(50);

my_list.PrintList();
```
Output
```output
NULL <-> [ 50 ] <-> [ 40 ] <-> [ 30 ] <-> [ 20 ] <-> [ 10 ] <-> NULL
```

## Function number 02
`void InsertAtEnd(element_type data)`  
Inserts the item at the end , it takes `O(n)`  
```cpp
clsDblLinkedList<int> my_list;
my_list.InsertAtEnd(10);
my_list.InsertAtEnd(20);
my_list.InsertAtEnd(30);
my_list.InsertAtEnd(40);
my_list.InsertAtEnd(50);

my_list.PrintList();
```
Output
```output
NULL <-> [ 10 ] <-> [ 20 ] <-> [ 30 ] <-> [ 40 ] <-> [ 50 ] <-> NULL
```

## Function number 03
`void DeleteFirstNode()`  
Deletes the first node in the list, it takes `O(1)`  
```cpp
clsDblLinkedList<int> my_list;
my_list.InsertAtEnd(10);
my_list.InsertAtEnd(20);
my_list.InsertAtEnd(30);
my_list.InsertAtEnd(40);
my_list.InsertAtEnd(50);
my_list.DeleteFirstNode();

my_list.PrintList();
```
Output
```output
NULL <-> [ 20 ] <-> [ 30 ] <-> [ 40 ] <-> [ 50 ] <-> NULL
```

## Function number 04
`void DeleteLastNode()`  
Deletes the last node in the list, it takes `O(n)`  
```cpp
clsDblLinkedList<int> my_list;
my_list.InsertAtEnd(10);
my_list.InsertAtEnd(20);
my_list.InsertAtEnd(30);
my_list.InsertAtEnd(40);
my_list.InsertAtEnd(50);
my_list.DeleteLastNode();

my_list.PrintList();
```
Output
```output
NULL <-> [ 10 ] <-> [ 20 ] <-> [ 30 ] <-> [ 40 ] <-> NULL
```

## Function number 05, 06, and 07
`int Size()`, it takes `O(1)`  
`bool IsEmpty()`, it takes `O(1)`  
`void Clear()`, clears the list from the heap, it takes `O(n)`    
```cpp
clsDblLinkedList<int> my_list;
my_list.InsertAtEnd(10);
my_list.InsertAtEnd(20);
my_list.InsertAtEnd(30);
my_list.InsertAtEnd(40);
my_list.InsertAtEnd(50);

cout << "Size : " << my_list.Size() << "\n";
cout << "Empty : " << my_list.IsEmpty() << "\n";
my_list.PrintList();
my_list.Clear();
my_list.PrintList();
```
Output
```output
Size : 5
Empty : 0
NULL <-> [ 10 ] <-> [ 20 ] <-> [ 30 ] <-> [ 40 ] <-> [ 50 ] <-> NULL
NULL <-> NULL
```

## Function number 08
`void DeleteNode(element_type data)`   
Deletes the first occurrence, it takes `O(n)`  
```cpp
clsDblLinkedList<int> my_list;
my_list.InsertAtEnd(10);
my_list.InsertAtEnd(20);
my_list.InsertAtEnd(30);
my_list.InsertAtEnd(40);
my_list.InsertAtEnd(50);

my_list.PrintList();
my_list.DeleteNode(30);
my_list.PrintList();
```
Output
```output
NULL <-> [ 10 ] <-> [ 20 ] <-> [ 30 ] <-> [ 40 ] <-> [ 50 ] <-> NULL
NULL <-> [ 10 ] <-> [ 20 ] <-> [ 40 ] <-> [ 50 ] <-> NULL
```

## Function number 09
`void Reverse()`  
Reverses a list, it takes `O(n)`  
```cpp
clsDblLinkedList<int> my_list;
my_list.InsertAtEnd(10);
my_list.InsertAtEnd(20);
my_list.InsertAtEnd(30);
my_list.InsertAtEnd(40);
my_list.InsertAtEnd(50);

my_list.PrintList();
my_list.Reverse();
my_list.PrintList();
```
Output
```output
NULL <-> [ 10 ] <-> [ 20 ] <-> [ 30 ] <-> [ 40 ] <-> [ 50 ] <-> NULL
NULL <-> [ 50 ] <-> [ 40 ] <-> [ 30 ] <-> [ 20 ] <-> [ 10 ] <-> NULL
```
## Function number 10
`Node* Find(element_type data)`  
Finds and returns a node by its value, it takes `O(n)`  
```cpp
clsDblLinkedList<int> my_list;
my_list.InsertAtEnd(10);
my_list.InsertAtEnd(20);
my_list.InsertAtEnd(30);
my_list.InsertAtEnd(40);
my_list.InsertAtEnd(50);

clsDblLinkedList<int>::Node* node = my_list.Find(10);
clsDblLinkedList<int>::Node* node1 = my_list.Find(11);

if (node) cout << "10 exists" << "\n";
else cout << "10 doesn't exist" << "\n";

if (node1) cout << "11 exists" << "\n";
else cout << "11 doesn't exist" << "\n";
```
Output
```output
10 exists
11 doesn't exist
```
## Function number 11
`Node* GetNode(int index)`   
Finds and returns a node by its index, it takes `O(n)`  
```cpp
clsDblLinkedList<int> my_list;
my_list.InsertAtEnd(10);
my_list.InsertAtEnd(20);
my_list.InsertAtEnd(30);
my_list.InsertAtEnd(40);
my_list.InsertAtEnd(50);

clsDblLinkedList<int>::Node* node = my_list.GetNode(2);

if (node) cout << node->data << "\n";
else cout << "Node doesn't exist" << "\n";
```
Output
```output
30
```
## Function number 12, and 13
`void InsertAfter(Node* node, element_type data)`  
`bool InsertAfter(int index, element_type data)`  
Insert a node after another node, it takes `O(n)`  
```cpp
clsDblLinkedList<int> my_list;
my_list.InsertAtEnd(10);
my_list.InsertAtEnd(20);
my_list.InsertAtEnd(30);
my_list.InsertAtEnd(40);
my_list.InsertAtEnd(50);

clsDblLinkedList<int>::Node* node = my_list.GetNode(2);

my_list.InsertAfter(node, 1000);
my_list.InsertAfter(2, 1111);

my_list.PrintList();
```
Output
```output
NULL <-> [ 10 ] <-> [ 20 ] <-> [ 30 ] <-> [ 1111 ] <-> [ 1000 ] <-> [ 40 ] <-> [ 50 ] <-> NULL
```
## Function number 14
`element_type GetItem(int index)`  
Find and returns the value of a node, it takes `O(n)`  
```cpp
clsDblLinkedList<int> my_list;
my_list.InsertAtEnd(10);
my_list.InsertAtEnd(20);
my_list.InsertAtEnd(30);
my_list.InsertAtEnd(40);
my_list.InsertAtEnd(50);

cout << my_list.GetItem(2) << "\n";
```
Output
```output
30
```
## Function number 15
`bool UpdateItem(int index, element_type data)`  
Updates the value of a node by its index, it takes `O(n)`
```cpp
clsDblLinkedList<int> my_list;
my_list.InsertAtEnd(10);
my_list.InsertAtEnd(20);
my_list.InsertAtEnd(30);
my_list.InsertAtEnd(40);
my_list.InsertAtEnd(50);

my_list.PrintList();
my_list.UpdateItem(2, 3000);
my_list.PrintList();
```
Output
```output
NULL <-> [ 10 ] <-> [ 20 ] <-> [ 30 ] <-> [ 40 ] <-> [ 50 ] <-> NULL
NULL <-> [ 10 ] <-> [ 20 ] <-> [ 3000 ] <-> [ 40 ] <-> [ 50 ] <-> NULL
```