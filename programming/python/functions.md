= functions =

print("hello")
str(3) == "3"
int("15") == 15
username = intput("enter your name: ")

* function
def add_numbers(a, b):
  print(a + b)

* type hinting: gives indication to compiler and IDEs about types
def add_numbers(a: int, b: int) -> int:
  return a + b

* return statement
def get_number():
  return 2

* arguments
students[]
def add_student(name, student_id=332)
    student = {"name": name, "student_id":student_id}
    students.append(student)

add_student("Brij")
add_student("Piyush", 15)
add_student(name="Pranav", student_id=15)

* variable number of arguments
def var_args(name, *args):
    print(name)
    print(args)

var_args("Piyush", "Pranav", "Brij")

* keyword args (named variable arguments)
def var_args(name, **kargs):
    print(name)
    print(kargs["description"], kargs["feedback"])

var_args("Brij", description="Loves Python", feedback=None)


* nested functions
def get_students():
    students = ["Piyush", "Pranav"]
    def get_students_titlecase()
        students_titlecase = []
        for student in students:
            students_titlecase.append(student.title())
        return student_titlecase
    students_titlecase_names = get_students_titlecase()
    print(students_titlecase_names)

Use nested functions when you don't need the logic anywhere else in your code, thereby not polluting your code.
Nested functions can access variables from outer function, this is called closure.
