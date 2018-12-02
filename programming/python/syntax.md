= Lexical Structure =
* # comment
* end of physical line marks the end of most statements
You can join two physical lines into a logical line by ending the first line with a backslash (\). Lines after first line are called continuation lines.
Python joins adjacent physical lines if the first line has open parenthesis like (, {, [
Triple-quoted string literals span physical lines.
Indentation issues apply to the first physical line of each logical line.
Python uses indentation to express the block structure of a program.
The first statement in a source file must have no indentation.

Standard Python style is to use 4 spaces per indentation level.

v3 source file can use any Unicode character encoded as UTF-8.

You can tell Python to use non-standard encoding by adding first line as comment (coding directive or encoding declaration):
# coding: iso-8859-1

* case-sensitive

* start class names with uppercase letter and other identifiers with a lowercase letter.
* start private identifier with _
* strat strongly private identifier with double __
* ' and " surround string literals

* Variable
In Python, there are no "declarations". The existence of a variable begins with a statement that binds the variable (assignment).
You can also unbind a variable, resetting the name so it no longer holds a reference (del statement).
Global variable: attribute of a module object
Local variable: lives in a function's local namespace

* assignment
plain assignment:
a = 2
a = b = c = 0 # a,b,c are assigned 0
a,b,c = x # x has to be iterable, first items is assigned to a, second to b, so on. (unpacking assignment)
a,b = b,a # same as unpacking assignment. Here it swaps the values
first, *middle, last = x # x is a list. first, middle, last = x[0], x[1:-1], x[-1] . Extended unpacking

* augmented assignment / in-place assignment
uses augmented operator, which is binary operator followed by =. The target must already be bound
+=, -=, *=, /=, etc.
x+=y # x=x.__iadd__(y)


x=x+y : does not modify the object to which name x was originally bound. It rebinds the name x to refer to a new object.
x+=y : modifies the object to which name x is bound when that object has special method __iadd__; otherwise it rebinds the name x to a new object, just like x=x+y

* del statements
unbinds references (does not delete objects)

* slicing
obj[start:stop]
obj[start:stop:stride]
obj[:stop]
obj[:stop:]
obj[None:stop:None]

* generating random number
import random

randomNumber = random.randrange(0, 10);

* loops
while True:


* conditional constructs
if a == '':
  break

elif a == 'a':
  print('a')

* input / output
print() # prints blank line
varableName = input('enter your name')
