= programming terms =

* Spaghetti code
Global variables (created in the main program code of python) can legally be used inside functions. However, it is strongly recommended to never do this. Using global variables inside functions leads to a poor coding practice called spaghetti code, where these variables can be used and modified all over a program. This style of programming makes the code very hard to understand and extremely difficult to maintain and modify, because any call to any function might change one or more global variables.
