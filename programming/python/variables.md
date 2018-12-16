= variable =

In Python, there are no "declarations". The existence of a variable begins with a statement that binds the variable (assignment).

myvariable = 42;
name = "hello"

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
You can also unbind a variable, resetting the name so it no longer holds a reference (del statement).
unbinds references (does not delete objects)

