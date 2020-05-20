# Programming Basics questions

## Computer science

### Data structures

#### What is the purpose of a list (array in some programming languages) data structure? Name some methods of it!
Collection which is ordered, changeable, allows duplicate members. Methods: .append(), .count(), .sort()
(link : https://www.programiz.com/python-programming/methods/list)


#### What is the difference between a list and a set?

SET: A set is a collection which is unordered and unindexed, and doesnt allow duplicates. Python, sets are written with curly brackets.
LIST: A list is a collection which is ordered and changeable. In Python lists are written with square brackets.


#### What is the purpose and methods of a map data structure?

MAP: Python map() function is used to apply a function on all the elements of specified iterable and return map object. Python map object is an iterator, so we can iterate over its elements. We can also convert map object to sequence objects such as list, tuple etc. using their factory functions.
EXAMPLE: map(function, iterable, ...)

A map (also known as dictionary or associative array) is not a data structure. It is an abstract data type: an interface that specifies what operations can be performed, but not how these operations are implemented.A map stores a collection of (key,value) pairs, such that each possible key appears at most once in the collection. The operations supported by a map are to store a new (key,value) pair, or to look up the value that is associated with a certain key.


### Algorithms

#### Fibonacci sequences. Write a method (or pseudo code), that generates the Fibonacci sequences.

EXAMPLE: The next number is found by adding up the two numbers before it: 0, 1, 1, 2, 3, 5, 8, 13, 21, 34, ...

def Fibonacci(n):
    if n<0:
        print("Incorrect input")
    # First Fibonacci number is 0
    elif n==0:
        return 0
    # Second Fibonacci number is 1
    elif n==1:
        return 1
    else:
        return Fibonacci(n-1)+Fibonacci(n-2)


#### How do you find a max value in a list/array if you can’t use any built-in functions?

lst = [1,9,6,5,4,...]
max = 0
for i in lst:
    if i > max:
        max = i
print(max)

#### How do you find the average of values in a list/array if you can’t use any built-in functions?

lst = [1,9,7,3,2]
n = 0
count = 0
for i in lst:
    n = n+i
    count += 1
average = n/count
return average

#### What do we call an *in-place* sort?

An in-place sorting algorithm uses constant extra space for producing the output (modifies the given list only). It sorts the list only by modifying the order of the elements within the list.

#### Explain an algorithm which sorts a list!
BUBBLE SORT:It is a comparison-based algorithm in which each pair of adjacent elements is compared and the elements are swapped if they are not in order.

list = [19,2,31,45,6,11,121,27]
bubblesort(list)
print(list)

[2, 6, 11, 19, 27, 31, 45, 121]

### Programming paradigms - procedural

#### What is the call stack?
https://dev.to/theoutlander/implementing-the-stack-data-structure-in-javascript-4164
#### What is “Stack overflow”?
An undesirable condition in which a particular computer program tries to use more memory space than the call stack has aviable.
#### What are the main parts of a function?

def random(arg1, arg2): # function signature (function name,paramater list)
    x = arg1+ arg2 # function body
    return x

### Programming languages - Python  
#### How do you use a dictionary in Python?
#### What does it mean that an object is immutable in Python?
#### What is conditional expression in Python?
#### What are different types of arguments in Python?
#### What is variable shadowing? (context: variable scope)
#### What can happen if you try to delete/drop/add an item from a List, while you are iterating over it in Python?
#### What is the "golden rule" of variable scoping in Python (context: LEGB)? What is the lifetime of variables?
#### If you need to access the iterator variable after a for loop, how would you do it in Python?
#### What type of elements can a list contain in Python?
#### What is slice operator in Python and how to use?
#### What arithmetic operators (+,*,-,/) can be used on lists in Python? What do they do?
#### What is the purpose of the in and not in membership operators in Python?
#### What does the + operator mean when used with strings in Python?
#### Explain f strings in Python?
#### Name 4 iterable types in Python!
#### What is the difference between list/set/dictionary comprehension and a generator expression in Python?
#### Does the order of the function definitions matter in Python? Why?
#### What does unpacking mean in Python?
#### What happens when you try to assign the result of a function which has no return statement to a variable in Python?

## Software engineering

### Debugging

#### What techniques can you use while debugging a program in Python?
#### What does step over, step into and step out mean while using the debugger?
#### How can you start to debug a program from a certain line using the debugger?

### Version control

#### What are the advantages of using a version control system?
#### What is the difference between the working directory, the staging area and the repository in git?
#### What are remote repositories in git?
#### Why does a merge conflict occur?
#### Through what series of commands could you put a new file into a remote repository connected to your existing local repository?
#### What does it mean atomic commits and descriptive commit messages?
#### What’s the difference between git and GitHub?

## Software design

### Clean code

#### What does clean code mean?
#### What steps do we usually do during a clean code refactoring?

### Error handling

#### What is exception handling?
#### What are the basics of exception handling in Python?
#### In which case should we catch an exception? Why?
#### What can/should we do with an exception in the ‘except’ block?
#### What does the else and finally statement do in a try-except block in Python?

## Software Development Methodologies

#### What is the main goal of a retrospective meeting?

## Programming environment

### Unix

#### What is UNIX and what is Linux?
#### What do we call the shell in Linux?
#### What does root means in a Linux environment?
#### How do you access your personal files in Linux?
#### How can you install an application in Linux?
#### What is package management in Linux, what are repositories?
#### How do you navigate in the filesystem with the command line?
#### What does the following commands do: mkdir, rm, cat, cp, touch?
#### How can you look up what does a command do in Linux if you have no internet connection?
#### What does the following commands do: head, tail, more, less?
#### How do you download a file from internet using the terminal?
