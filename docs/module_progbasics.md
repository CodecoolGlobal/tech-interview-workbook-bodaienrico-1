# Programming Basics questions
-------------------
## Computer science
-------------------
### Data structures

#### What is the purpose of a list (array in some programming languages) data structure? Name some methods of it!
collection which is ordered, changeable, allows duplicate members
1. **list():** creates a list in Python. **list([iterable])**
2. **append():** Add a single element to the end of the list. **list.append(item)**
3. **extend():** Add Elements of a List to Another List. **list1.extend(list2)**
4. **insert():** Inserts Element to The List.- **list.insert(index, element)**
5. **remove():** Removes item from the list. **list.remove(element)**
6. **clear():** Removes all Items from the List. **list.clear()**
7. **index():** returns smallest index of element in list. **list.index(element**)
8. **count():** Removes element at the given index. **list.count(element)**
9. **reverse():** Reverses a List. **list.reverse()**
10. **reversed():** returns the reversed iterator of a sequence. **reversed(seq)**
11. **sort():** sorts elements of a list. **list.sort(key=..., reverse=...)**
12. **sorted** returns a sorted list from the given iterable. **sorted(iterable, key=None, reverse=False)**
13. **copy():** Returns Shallow Copy of a List. =
14. **any():** Checks if any Element of an Iterable is True. **any(iterable)**
15. **all():** Returns true when all elements in iterable is true. **all(iterable)**
16. **ascii():** Returns String Containing Printable Representation. **ascii(object)**
17. **bool():** Converts a Value to Boolean. **bool([value])**
18. **enumerate():** Returns an Enumerate Object. **enumerate(iterable, start=0)**
19. **filter():** constructs iterator from elements which are true. **filter(function, iterable)**
20. **iter():** returns an iterator. **iter(object, sentinel)**
21. **len():** Returns Length of an Object. **len(s)**
22. **max():** returns the largest item. **max(iterable, *iterables, key, default)**
23. **min():** returns the smallest value. **min(iterable, *iterables, key, default)**
24. **map():** Applies Function and Returns a List. **map(function, iterable, ...)**
25. **slice():** returns a slice object. **slice(start, stop, step)**
26. **sum():** Adds items of an Iterable. **sum(iterable, start)**
27. **zip():** Returns an iterator of tuples. **zip(*iterables)**
#### What is the difference between a list/array and a set?
>set:A set is a collection which is unordered and unindexed, and doesnt allow duplicates.
>
>list/array: ordered, can have multiple occurences of the same element
>
>list vs set: duplication, order, index
#### What is the purpose and methods of a dictionary/map data structure?

[source](https://www.geeksforgeeks.org/python-map-function/)

_A map (also known as dictionary or associative array) is **not a data structure**. It is an abstract data type: an interface that specifies what operations can be performed, but not how these operations are implemented. A map stores a collection of (key,value) pairs, such that each possible key appears at most once in the collection. The operations supported by a map are to store a new (key,value) pair, or to look up the value that is associated with a certain key._
```python
def calculateSquare(n):
	return n*n

numbers = (1, 2, 3, 4)
result = map(calculateSquare, numbers)
print(result)
```
### Algorithms

#### Fibonacci sequences. Write a method (or pseudo code), that generates the Fibonacci sequences.
>[source](https://www.mathsisfun.com/numbers/fibonacci-sequence.html)
>[source](https://www.geeksforgeeks.org/python-program-for-program-for-fibonacci-numbers-2/)

xn = xn−1 + xn−2

```python
def Fibonacci(n):
    if n<0:
        print("Incorrect input")
    elif n==0:
        return 0
    elif n==1:
        return 1
    else:
        return Fibonacci(n-1)+Fibonacci(n-2)
```		

#### How do you find a max value in a list/array if you can’t use any built-in functions?
1. sort method
2. print the last element in a list
```python
def find_max():
    lst = [1, 9, 7, 3, - 2]
    max = 0
    for i in lst:
        if i > max:
            max = i
    return max
```	

#### How do you find the average of values in a list/array if you can’t use any built-in functions?
1. add elements to eachother
2. count them with a variable
3. add divide them by a variable
```python
def find_avg():
    lst = [1, 9, 7, 3, - 2]
    count = 0
    sum = 0
    for i in lst:
        count += 1
        sum = sum  + i
    avg = sum/count
    return avg
```	

#### What do we call an *in-place* sort?
An in-place sorting algorithm uses constant extra space for producing the output (modifies the given list only). It sorts the list only by modifying the order of the elements within the list.

#### Explain an algorithm which sorts a list!

[source](https://www.tutorialspoint.com/python_data_structure/python_sorting_algorithms.htm)

1. **Bubble sort**:_sometimes referred to as sinking sort, is a simple sorting algorithm that repeatedly steps through the list, compares adjacent elements and swaps them if they are in the wrong order. The pass through the list is repeated until the list is sorted. The algorithm, which is a comparison sort, is named for the way smaller or larger elements "bubble" to the top of the list._
```python
lst = [19,2,31,45,6,11,121,27]
def bubblesort(lst):
    for num in range(len(lst)-1,0,-1):
        for index in range(num):
            if lst[index]>lst[index+1]:
                temp = lst[index]
                lst[index] = lst[index+1]
                lst[index+1] = temp
bubblesort(lst)
print(lst)
```

### Programming paradigms - procedural

#### What is the call stack?
call stack: is what a program uses to keep track of function calls. The call stack is made up of stack frames - one for each function call.
![ ](https://camo.githubusercontent.com/e83d69b5c62679df5aeaaaf7f13a02a90f29b5f4/68747470733a2f2f7265732e636c6f7564696e6172792e636f6d2f70726163746963616c6465762f696d6167652f66657463682f732d2d733151626c3847662d2d2f635f6c696d6974253243665f6175746f253243666c5f70726f6772657373697665253243715f6175746f253243775f3838302f68747470733a2f2f74686570726163746963616c6465762e73332e616d617a6f6e6177732e636f6d2f692f6d776377726530397331327671613367766c37612e706e67)
#### What is “Stack overflow”?
error type
>
_In software, a stack overflow occurs if the call stack pointer exceeds the stack bound. The call stack may consist of a limited amount of address space, often determined at the start of the program. The size of the call stack depends on many factors, including the programming language, machine architecture, multi-threading, and amount of available memory. When a program attempts to use more space than is available on the call stack (that is, when it attempts to access memory beyond the call stack's bounds, which is essentially a buffer overflow), the stack is said to overflow, typically resulting in a program crash. fe: recursive function never quit._
#### What are the main parts of a function?
```python
def random(arg1, arg2): # function signature(function name,paramater list)
    multiply = arg1+ arg2 # function body
    return multiply
```	

### Programming languages - Python  
#### How do you use a dictionary in Python?
[source](https://www.w3schools.com/python/python_dictionaries.asp)

_A dictionary is a collection which is unordered, changeable and indexed. In Python dictionaries are written with curly brackets, and they have keys and values._ dict_name = {key:value, ... keyN:valueN}
#### What does it mean that an object is immutable in Python?
_These are of in-built types like int, float, bool, string, unicode, tuple. An immutable object can't be changed after it is created._
#### What is conditional expression in Python?
expression that returns value A or B depending on wether a Boolean value is true or false
>
Ternary operators also known as conditional expressions are operators that evaluate something based on a condition being true or false. Details: value_if_true if statement else value_if_false

#### What are different types of arguments in Python?
[source](http://www.trytoprogram.com/python-programming/python-function-arguments/)
1. **Default Arguments**: _def sum(a=4, b=2):_
2. **Keyword Arguments**: *def print_name(name1, name2): print_name(name2 = 'John',name1 = 'Gary')*
3. **Variable-length Arguments**: _def display(*name, **address): display('john','Mary','Nina',John='LA',Mary='NY',Nina='DC') *(args) - Arguents, **(KWargs) (Key Word Arguments)_
#### What is variable shadowing? (context: variable scope)
In computer programming, variable shadowing occurs when a variable declared within a certain scope (decision block, method, or inner class) has the same name as a variable declared in an outer scope. At the level of identifiers (names, rather than variables), this is known as name masking.
>
_(It's defined as when a variable "hides" another variable with the same name. So, when variable shadowing occurs, there are two or more variables with the same name, and their definitions are dependent on their scope (meaning their values may be different depending upon scope)._
#### What can happen if you try to delete/drop/add an item from a List, while you are iterating over it in Python?
[source](https://www.quora.com/In-Python-why-cant-you-remove-elements-from-a-list-with-a-for-loop-but-you-can-with-a-while-loop)
>
_When we delete an item from the list the for loop will be skip some element, because we changed the list(indexing). When we add an item to the list the for loop will be forever running._
#### What is the "golden rule" of variable, scoping in Python (context: LEGB)? What is the lifetime of variables?
[source](https://www.geeksforgeeks.org/scope-resolution-in-python-legb-rule/)
In Python, the LEGB rule is used to decide the order in which the namespaces are to be searched for scope resolution. The scopes are listed below in terms of hierarchy (highest to lowest/narrowest to broadest):
>1. **Local(L)**: _Defined inside function/class_
>2. **Enclosed(E)**: _Defined inside enclosing functions(Nested function concept)_
>3. **Global(G)**: _Defined at the uppermost/global level._
>4. **Built-in(B)**: _Reserved names in Python builtin modules_
#### If you need to access the iterator variable after a for loop, how would you do it in Python?
[source](https://realpython.com/python-for-loop/)

Never your it after **NEVER**
>
**iterator type:**
1. **String**: _iter('foobar')_
2. **List**: _iter(['foo', 'bar', 'baz'])_
3. **Tuple** _iter(('foo', 'bar', 'baz'))_
4. **Set** _iter({'foo', 'bar', 'baz'})_
5. **Dict** _iter({'foo': 1, 'bar': 2, 'baz': 3})_
>
**Can't be iterator:**
1. **Integer** _iter(42) TypeError: 'int' object is not iterable_
2. **Float** _iter(3.1) TypeError: 'float' object is not iterable_
3. **Built-in function** _iter(len) TypeError: 'builtin_function_or_method' object is not iterable_
#### What type of elements can a list contain in Python?
Each item in a python list can be of any data type. fe: string, numbers, list, tuple, dict
#### What is slice operator in Python and how to use?
[source](https://www.w3schools.com/python/ref_func_slice.asp)
>
The **slice()** function returns a slice object. _slice(start, end, step)_
```python
a[start:stop:step]
a[slice(start, stop, step)]
```
>
**list slicing**: list: listname[0:2] [:4] [1:-1] [:]
#### What arithmetic operators (+,*,-,/) can be used on lists in Python? What do they do?
[source](https://www.programiz.com/python-programming/operators)
>
```python
NumList1 = [10, 20, 30]
NumList2 = [5, 2, 3]
add = []
sub = []
multi = []
div = []
mod = []
expo = []

for j in range(3):
    add.append( NumList1[j] + NumList2[j])
    sub.append( NumList1[j] - NumList2[j])
    multi.append( NumList1[j] * NumList2[j])
    div.append( NumList1[j] / NumList2[j])
    mod.append( NumList1[j] % NumList2[j])
    expo.append( NumList1[j] ** NumList2[j])

print("\nThe List Items after Addition =  ", add)
print("The List Items after Subtraction =  ", sub)
print("The List Items after Multiplication =  ", multi)
print("The List Items after Division =  ", div)
print("The List Items after Modulus =  ", mod)
print("The List Items after Exponent =  ", expo)

output:
The List Items after Addition =   [15, 22, 33]
The List Items after Subtraction =   [5, 18, 27]
The List Items after Multiplication =   [50, 40, 90]
The List Items after Division =   [2.0, 10.0, 10.0]
The List Items after Modulus =   [0, 0, 0]
The List Items after Exponent =   [100000, 400, 27000]
```
#### What is the purpose of the in and not in membership operators in Python?
[source](https://www.geeksforgeeks.org/python-membership-identity-operators-not-not/)
>
Membership operators are operators used to validate the membership of a value. It test for membership in a sequence, such as strings, lists, or tuples.
>
**in operator** : _The ‘in’ operator is used to check if a value exists in a sequence or not. Evaluates to true if it finds a variable in the specified sequence and false otherwise._
>
**‘not in’ operator**: _Evaluates to true if it does not finds a variable in the specified sequence and false otherwise._
>

#### What does the + operator mean when used with strings in Python?
to explicitly concatenate the strings
>
fe: "spam" + "eggs" spameggs
#### Explain f strings in Python?
[source](https://realpython.com/python-f-strings/) [source](https://www.geeksforgeeks.org/formatted-string-literals-f-strings-python/)
>
Also called “formatted string literals,” f-strings are string literals that have an f at the beginning and curly braces containing expressions that will be replaced with their values. fe:
>
```python
answer = 456
f"Your answer is "{answer}""
```
#### Name 4 iterable types in Python!
1. list
2. strings
3. tuple
4. dictonory
#### What is the difference between list/set/dictionary comprehension and a generator expression in Python?
[source](https://www.geeksforgeeks.org/python-list-comprehensions-vs-generator-expressions/)
>
**List Comprehension**: _It is an elegant way of defining and creating a list. List Comprehension allows us to create a list using for loop with lesser code. What normally takes 3-4 lines of code, can be compressed into just a single line._
```python
  values = [ expression
             for value in collection
             <if condition> ]
```
```python
a_dict = {key: value  for key, value in zip(list1, list2) if clause}
```             
>
**Generator Expressions**: _similar to list comprehensions, but instead of creating a list and keeping the whole sequence in the memory, the generator generates the next element in demand and allows us to create a generator without the yield keyword._
>
```python
genexpr = ('Hello' for i in range(3))
```
>
>**List Comprehension vs Generator Expressions:**
>
>The generator yields one item at a time and generates item only when in demand. Whereas, in a list comprehension, Python reserves memory for the whole list. Thus we can say that the generator expressions are memory efficient than the lists.
>
#### Does the order of the function definitions matter in Python? Why?
Really, a python source code is a list of instructions from top of file to bottom. Instructions are executed in order.
#### What does unpacking mean in Python?
[source](https://stackabuse.com/unpacking-in-python-beyond-parallel-assignment/)
>
Unpacking in Python refers to an operation that consists of assigning an iterable of values to a tuple (or list ) of variables in a single assignment statement. As a complement, the term packing can be used when we collect several values in a single variable using the iterable unpacking operator.
```python
a, b, c = 1, 2, 3  
a, b, c = call_return_three()
```
#### What happens when you try to assign the result of a function which has no return statement to a variable in Python?
If there is no return statement (or just a return without an argument), an implicit **return None** is added to the end of a function.

## Software engineering

### Debugging

#### What techniques can you use while debugging a program in Python?
1. print
2. debugger
3. rubberduck _(explain code line-by-line)_
#### What does step over, step into and step out mean while using the debugger?
1. **step over**: _skip functions_
2. **step into**: _by default the debugger skips over managed properties and fields, but the Step Into Specific command allows you to override this behavior._
3. **step out**: _to step out the specific_
#### How can you start to debug a program from a certain line using the debugger?
1. breakpoints
2. Run to cursor

### Version control

#### What are the advantages of using a version control system?
[source](https://www.git-tower.com/learn/git/ebook/en/command-line/basics/why-use-version-control)
>
1. _Collaboration_
2. _Storing Versions (Properly)_
3. _Restoring Previous Versions_
4. _Understanding What Happened (commits)_
5. _Backup_

#### What is the difference between the working directory, the staging area and the repository in git?
[source](http://archaeogeek.github.io/foss4gukdontbeafraid/git/stages.html) [source](https://medium.com/@lucasmaurer/git-gud-the-working-tree-staging-area-and-local-repo-a1f0f4822018)
>
[](https://camo.githubusercontent.com/805666f761f7fa28ea2622d278e45229060b53df/68747470733a2f2f6e65757261746873626f61742e626c6f672f706f73742f6769742d696e74726f2f66656174757265642e706e67)
>
#### What are remote repositories in git?
[source](https://www.git-tower.com/learn/git/ebook/en/command-line/remote-repositories/introduction)
>
Only when it comes to sharing data with your teammates, a remote repo comes into play. Think of it like a "file server" that you use to exchange data with your colleagues.
#### Why does a merge conflict occur?
[source](https://www.atlassian.com/git/tutorials/using-branches/merge-conflicts) [source](https://dzone.com/articles/merge-conflict-everything-you-need-to-know)
>
1. _Merge incoming changes from remote branch to the local branch_
2. _Merge outgoing changes from local branch to the remote branch_
3. _Merge changes in one local branch to another local branch_
4. _Merge changes in one remote branch to another remote branch_
#### Through what series of commands could you put a new file into a remote repository connected to your existing local repository?
1. mv - move file to that repo
2. git add - add to repo
3. git commit
4. git push
#### What does it mean atomic commits and descriptive commit messages?
Atomic commits, in short, are what they sound like: atomic. I feel like there’s basically three features a commit needs to have to be atomic:
>
1. _Every commit pertains to one fix or feature_
2. _Don't break the build on any commit_
3. _Purpose is clear from commit msges and description (descriptive commit messages)_
>
#### What’s the difference between git and GitHub?
Git is a distributed **version control tool** that can manage a development project's source code history, while GitHub is a **cloud based platform** built around the Git tool.
## Software design

### Clean code

#### What does clean code mean?
writing readable and sustainable code
in the code there aren't: dead code; unneccesary or not used things, comments; func.s that do more than the name says; badly named func.s, var.s, etc; 
DRY: don't repeat yourself
naming things well, using naming conventions
being consistent
general rules: follow standars conventions; keep it simple stupid; leave the campground cleaner than you found it; always look for the root cause of a problem
name things properly; DRY; SRP(single responsibility principle); write modular code; avoid global var.s; avoid too many indentation levels; avoid too long func.s; write self-documenting code
#### What steps do we usually do during a clean code refactoring?
check for, rewrite/fix: 
bad names
bad formattings
repeated codes
long methods
wrong comment usage
dead code
magic numbers

### Error handling

#### What is exception handling?
handling exceptions>an event which occurs during the execution of a program that disrupts the normal flow of the program instructions.
when the script encounters a situation that it cannot cope > raises an exeption > it must be handled, else it terminates and quits
#### What are the basics of exception handling in Python?
try: block, except: statement, followed by a block of code
syntax errors, runtime errors, logival errors
#### In which case should we catch an exception? Why?
if we know that a particular section of our program is likely to cause an error, so we can tell what to do when it happens instead of letting the error crash our program. We can intercept it, do sg about it and allow the program to continue
#### What can/should we do with an exception in the ‘except’ block?
a code which handles the problem as elegantly as possible
e.g. except IOError: print('Error: cannot find file or read data')
#### What does the else and finally statement do in a try-except block in Python?
else:optional, when present must follow all except clauses. useful for code that must be executed if the try clause does not raise exception
finally: optional, define clean-up actions that must be executed under all circumstances. the finally clause execute as the last task before the try statement completes. it runs whether or not the try statement produces an exeption

## Software Development Methodologies

#### What is the main goal of a retrospective meeting?
to evaulate the past working cycle and define actions that may fix or improve things identified as negative

## Programming environment

### Unix

#### What is UNIX and what is Linux?
Unix: operating system, written in C. Allows quick modification, acceptance and portability. Proprietary operating system. Works on CLI (Command Line Interface). created in the late 1960s at AT&T Bell Labs.
Linux: operating system. Software which enables applications and the users to access the devices on the computer to perform some specific function. Linux OS relays instructions from an application from the computer's processor and sends the result back to the application via the Linus OS. Free and open source software collaboration. Built by Linus Torvalds at the University of Helsinki in 1991.

difference: 
Linux-Open Source <>Unix: the versions primarily developed by AT&T, 
Linux: portable and is booted from a USB Stick <> Unix: not portable, 
Linux:OS can be installed on various types of devices like mobile, tablet, computers <> Unix: OS is used for inernet servers, workstations & PCs
Linux: the source code is aviable to the general public <> Unix: source code is not aviable to anyone
-> Linux:source code is aviable to the general public <> Unix: source code is proprietary
Linux is a clone of Unix
Linux default shell is BASH <> Unix shell is Bourne Shell
Linux threat detection and solution are very fast <> Unix users require longer wait times to get the proper bug fixing patch
Important versions of Linux:Redhat, Ubuntu, OpenSuse, Solaris <> Unix: HP-UX, AIS, BSD, etc.
#### What do we call the shell in Linux?
is a program that takes commands from the keyboard and gives them to the operating system to perform. Command line interface(CLIs). On most Linux systems a program called BASH acts as the shell program. other shell programs:ksh, tcsh, zsh
#### What does root means in a Linux environment?
root: the user name or account that by default has access to all commands and files on a Linux OS. Also referred as the root account, root user and superuser.
#### How do you access your personal files in Linux?
#### How can you install an application in Linux?
sudo apt install appname(e.g. inkspace) in Ububtu
Fedora:instead of apt> dnf; OpenSUSE: yzpper; Debian: apt; Slackware: sbopkg; FreeBSD: pkg_add; OpenIndiana: pkg
(sudo apt search e.g.pyqt > sudo apt install e.g.python-qt5)
#### What is package management in Linux, what are repositories?
apt:(advanced packaging tool); > installing, upgrading software packages, updading of the package list index, upgradging the entire Ubuntu system
e.g.: sudo apt install nmap > install nmap package; sudo apt remove nmap > remove nmap package; sudo apt update >update package index; sudo apt upgrade > upgrade packages
repo.s: collection of packages found online or on physical media
#### How do you navigate in the filesystem with the command line?
pwd:>print working directory. show which dir. you're located 
ls: list files in current dir.
cd: change dir.s. 
cd/ navigate into the root dir.
cd or cd~ navigate to home dir.
cd .. navigate up one dir. level
cd - navigate to the previous dir.
mv: move a file to a different location or rename a file
#### What does the following commands do: mkdir, rm, cat, cp, touch?
mkdir: make directories
rm: remove files or directories
cat: concatenate and print files / create the file with content
cp: copy files and directories
touch: create file without any content. > empty file
#### How can you look up what does a command do in Linux if you have no internet connectionli?
man page > man man
#### What does the following commands do: head, tail, more, less?
head: print the top N number of data of the given input.  by default - first 10 lines
tail: output the last part of files
more: file perusal filter for crt viewing. filter for paging text one screenful at a time
less: opposite of more. 
#### How do s download a file from internet using the terminal?
wget "copy_url_here"
wget -P location "url">> downloed to the current dir.
wget -O location/NewFileName "url">> download to desktop
