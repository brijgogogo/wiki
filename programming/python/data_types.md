= Data types =
* Numbers: integers, floating point numbers, complex numbers
int and long in v2
In v3, there is no distinction between kinds of integers
All numbers in Python are immutable objects.
integers: decimal, binary, octal, hexadecimal

* Sequences
ordered container of items, indexed by integers
strings, tuples, lists

Iterables
All sequences are iterables.
bounded iterable: an iterable that eventually stops yeilding items

strings: sequence of characters
Strings are immutable.
v2: byte strings
v3: Unicode
Use quote or triple-quote. Quote can be escaped with backslash (\)
You can use \ to continue string in next line. Or you can use triple-quoted string.
In triple-quoted string literal, line breaks remain.

raw string: starts with r or R before quote. In raw string, escape sequences are not interpreted.

tuple:immutable ordered sequence of items.
A tuple with exactly 2 items is known as pair.
e.g:
(100, 200, 300)
(3.14,)         # tuple with 1 item
()               # empty tuple
tuple('wow') = ('w', 'o', 'w')

Lists: mutable ordered sequence of items
[42, 3.14, 'hello']
[100]
[] # Empty list
list('wow') = ['w', 'o', 'w']

Sets: to represent arbitrarily ordered collection of unique items
set: mutable, not hashable
frozenset: immutable, hashable
Items are not ordered.
{42, 3.14, 'hello'}
{100}
set() # empty set

dictionaries: arbitrary collection of objects indexed by nearly arbitrary values called keys.
Not necessarily ordered. Mappings are mutable.
Keys must be hashable.
{'x': 42, 'y': 14}
{1:2, 3:4}
{1: 'za', 'br':23}
{} # empty dictionary
dict(x=42, y=3)
dict([(1,2), (3.4)])
dict() # empty dictionary

* None
denotes a null object

* Callables
types whose instances support the function call operation

* Booleans
truth value: true or false
Any nonzero number or nonempty container (string, tuple, list, set, dictionary) is true.
0, None, empty containers are false.
bool(x) will return true when x is true.
The built-in type bool is a subclass of int. Its values are True and False (1, 0).

variable: a named memory location that holds a value
you create and give value to a varible with an assignment statement
<variable> = <expression>
= is assignment operator
age = 31
name = 'Brij'
alive = True
height = 5.7

naming conventions: camel case
