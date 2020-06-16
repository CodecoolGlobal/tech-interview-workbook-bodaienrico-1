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

`def calculateSquare(n):`
`	return n*n`

`numbers = (1, 2, 3, 4)`
`result = map(calculateSquare, numbers)`
`print(result)`

### Algorithms

#### Fibonacci sequences. Write a method (or pseudo code), that generates the Fibonacci sequences.
nums = 0,1,1,2,3,5,8......
new_num = adding up the previous 2 nums
def fibonacci(n):
	if n<0:
		print('wrong input')
	elif n ==0:
		return 0
	elif n ==1:
		return 1
	else:
		return fibonacci(n-1)+fibonacci(n-2)

#### How do you find a max value in a list/array if you can’t use any built-in functions?
e.g. 
lst = [1,9,7,3,-2]
max=0
for i in lst:
    if i > max:
        max = i
return max

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
> modify the list order
#### Explain an algorithm which sorts a list!
list = [19,2,31,45,6,11,121,27]
def bubblesort(lst):
    for num in range(len(list)-1,0,-1):
        for index in range(num):
            if list[index]>list[index+1]:
                temp = list[index]
                list[index] = list[index+1]
                list[index+1] = temp
bubblesort(lst)
print(lst)

### Programming paradigms - procedural

#### What is the call stack?
call stack: is what a program uses to keep track of function calls. The call stack is made up of stack frames - one for each function call.
#### What is “Stack overflow”?
1. an undesirable condition in which a particular computer program tries to use more memory space than the call stack has aviable.
2. a large, trusted online community for developers to learn, share their programming knowledge.
#### What are the main parts of a function?
header: begins with a keyword, ends with a colon
body:consisting of one or more Python statements, each indented the same amount from the header.

### Programming languages - Python  
#### How do you use a dictionary in Python?
dictname={'key': value}
var = dictname.get('key')
dictname['key'] = newvalue
dictname.values()
dictname.keys()
e.g. for k, v in dictname.items():
	print(k,v)
dictname['addkey'] = addvalue
del dictname['key'] > removes item
dictname.pop('key') > removes item
dictname.popitem() > removes last inserted item
dictname = dict(key1='value1', key2='value2')
#### What does it mean that an object is immutable in Python?
after created it cant't be changed, only reassigned
e.g. bool, int, float, tuple, str
#### What is conditional expression in Python?
expression that returns value A or B depending on wether a Boolean value is true or false
operators that evaluate sg based on a contition being true or false
#### What are different types of arguments in Python?
default arg. >> default value
keyword arg. >> values get assigned to the arg.s according to their position
arbitary / variable-length arg. >> *before parameter name, when we don't know in advance the number of arg.s
#### What is variable shadowing? (context: variable scope)
when a variable declared within a certain scope has the same name as a var. declared in an outer scope
#### What can happen if you try to delete/drop/add an item from a List, while you are iterating over it in Python?
e.g. list = [2, 3, 4], iterating in list range len , try to remove 2, > index error 
the length of the range and the lenght of the list not equal anymore
#### What is the "golden rule" of variable, scoping in Python (context: LEGB)? What is the lifetime of variables?
var. scope: the part of the program where the var. is accessible
var lifetime: the duration for which the var. exists
local var.: accessible from the point it is defined - until the end of the func., exist: as lon as the func.is executing
use global var. only if intended to us eglobally
LEGB: Local, Enclosing, Global, Built-in
Local: in func.
Enclosing: only for nested func.s
Global: global
Built-in: when run script, open interactive session > keywords, func.s, exceptions, etc.
Python searches L->B., if isn't found > error
> write self-contained func.s that rely on local names rather than global ones. Try to use unique object names, no matter what scope you're in. Avoid global name modifications and cross-module name modifications. Use global names as constants.
#### If you need to access the iterator variable after a for loop, how would you do it in Python?
save the value of it in a variable/list. Better if I don't need to.
#### What type of elements can a list contain in Python?
numeric types, text sequence
#### What is slice operator in Python and how to use?
slice(start, stop, step) >> slice a sequent
#### What arithmetic operators (+,*,-,/) can be used on lists in Python? What do they do?
+,- > add/substract one list to the other e.g. lst1= [1,2] lst2 = [3,4] lst3 = lst1 + lst2 
#### What is the purpose of the in and not in membership operators in Python?
test for membership in a sequence.
in: evaulates to True if it finds a var. in the specified sequence, False otherwise.
not in: evaluates to True if it does not finds a var. in the specified sequence, False otherwise.
#### What does the + operator mean when used with strings in Python?
e.g. str1 = 'abc' str2='def' str1+str2 = 'abcdef'
#### Explain f strings in Python?
formatted string literal / f-string
may contain replecament fields > expressions delimited by curly braces >> {}
formatted strings are really expressions evaulated at run time
the parts of the string outside curly braces are treated literally
#### Name 4 iterable types in Python!
list, tuple, string, dictionary, set
#### What is the difference between list/set/dictionary comprehension and a generator expression in Python?
generator: size of the object is smaller, type of resulting values: generator. cannot access an element by index.
e.g. g = (n*2 for n in range(1000))
both: can iterate over
#### Does the order of the function definitions matter in Python? Why?
yes; Python can't find a name that just doesn't exist yet > e.g. row1: def print_sum(a,b):
	print(sum_nums(a,b)) and sum_nums defined in row4 > name error
#### What does unpacking mean in Python?
* > unpack the list >>all elements of it can be passed as different parameters
e.g. def func(a, b, c, d):
	print(a, b, c, d)
lst = [1, 2, 3, 4]
func(*lst)
>>> (1, 2, 3, 4)
** for dicts
> can give a list for args. in a func.
#### What happens when you try to assign the result of a function which has no return statement to a variable in Python?
you get none

## Software engineering

### Debugging

#### What techniques can you use while debugging a program in Python?
debugger, print, rubber duck >explain code line-by-line
#### What does step over, step into and step out mean while using the debugger?
step over: step to the next
step into: step into the func., step out: step out from the func.
#### How can you start to debug a program from a certain line using the debugger?
put down a breakpoint to that line

### Version control

#### What are the advantages of using a version control system?
it's a way of stroring informaton about changes in code > keep track of every modification to the code, including the person responsible for it and precise time
#### What is the difference between the working directory, the staging area and the repository in git?
working dir. >git add > staging area > git commit >repo
working dir: where you currently working. if you not save sg you will lose it > 'untracked' area of git
staging area: where git starts tracking and saving changes that occur in files
repo: all of your checkpoints or commits. this area saves everything
#### What are remote repositories in git?
remote repo.s: versions of your project that are hosted on the internet or network somewhere
#### Why does a merge conflict occur?
git cannot automatically determinate what is correct beacuse: 2people have chaned the same lines in a file / A deleted a file while while B was modifying it / not start merging if git sees there are changes in the working dir or staging area of the current project >pending changes could be written over by the commits that are being merged
#### Through what series of commands could you put a new file into a remote repository connected to your existing local repository?
git add, git commit, git push
#### What does it mean atomic commits and descriptive commit messages?
atomic: one fix or feature
descriptive: short 50 chars or less summary of changes; one blank line; a detailed explanatory text if neccessary(72 char)
#### What’s the difference between git and GitHub?
git: version control software
github: git repo. hosting server which offers all the source code management provided in git. > where you upload your git repo.

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
