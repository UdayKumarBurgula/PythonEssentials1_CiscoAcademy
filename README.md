"# PythonEssentials1_CiscoAcademy" 




CPython is the original (traditional) Python language implementation written in the C language, as opposed to other, non-default implementations, such as Jython, implemented in the Java language, which came later. CPython is the Python language implementation available for download from www.python.org, and the first to adopt new features that come with all the subsequent Python versions.

A Python console is a command-line interpreter that allows you to execute Python commands, instructions, and scripts line by line. Just like the one here: www.python.org/shell.

function_name(argument)


Let's see:
First, Python checks if the name specified is legal (it browses its internal data in order to find an existing function of the name; if this search fails, Python aborts the code)
second, Python checks if the function's requirements for the number of arguments allows you to invoke the function in this way (e.g., if a specific function demands exactly two arguments, any invocation delivering only one argument will be considered erroneous, and will abort the code's execution)
third, Python leaves your code for a moment and jumps into the function you want to invoke; of course, it takes your argument(s) too and passes it/them to the function;
fourth, the function executes its code, causes the desired effect (if any), evaluates the desired result(s) (if any) and finishes its task;
finally, Python returns to your code (to the place just after the invocation) and resumes its execution.







2.1.14 SECTION SUMMARY
1. The print() function is a built-in function. It prints/outputs a specified message to the screen/console window.
2. Built-in functions, contrary to user-defined functions, are always available and don't have to be imported. Python 3.8 comes with 69 built-in functions. You can find their full list provided in alphabetical order in the Python Standard Library.
3. To call a function (this process is known as function invocation or function call), you need to use the function name followed by parentheses. You can pass arguments into a function by placing them inside the parentheses. You must separate arguments with a comma, e.g., print("Hello,", "world!"). An "empty" print() function outputs an empty line to the screen.
4. Python strings are delimited with quotes, e.g., "I am a string" (double quotes), or 'I am a string, too' (single quotes).
5. Computer programs are collections of instructions. An instruction is a command to perform a specific task when executed, e.g., to print a certain message to the screen.
6. In Python strings the backslash (\) is a special character which announces that the next character has a different meaning, e.g., \n (the newline character) starts a new output line.
7. Positional arguments are the ones whose meaning is dictated by their position, e.g., the second argument is outputted after the first, the third is outputted after the second, etc.
8. Keyword arguments are the ones whose meaning is not dictated by their location, but by a special word (keyword) used to identify them.
9. The end and sep parameters can be used for formatting the output of the print() function. The sep parameter specifies the separator between the outputted arguments, e.g., print("H", "E", "L", "L", "O", sep="-"), whereas the end parameter specifies what to print at the end of the print statement.
10. Print “2” times - print("     *     *     "*2)   

2 
1. Literals are notations for representing some fixed values in code. Python has various types of literals - for example, a literal can be a number (numeric literals, e.g., 123), or a string (string literals, e.g., "I am a literal.").
2. The binary system is a system of numbers that employs 2 as the base. Therefore, a binary number is made up of 0s and 1s only, e.g., 1010 is 10 in decimal.
Octal and hexadecimal numeration systems, similarly, employ 8 and 16 as their bases respectively. The hexadecimal system uses the decimal numbers and six extra letters.
3. Integers (or simply ints) are one of the numerical types supported by Python. They are numbers written without a fractional component, e.g., 256, or -1 (negative integers).
4. Floating-point numbers (or simply floats) are another one of the numerical types supported by Python. They are numbers that contain (or are able to contain) a fractional component, e.g., 1.27.
5. To encode an apostrophe or a quote inside a string, you can either use the escape character, e.g., 'I\'m happy.', or open and close the string using an opposite set of symbols to the ones you wish to encode, e.g., "I'm happy." to encode an apostrophe, and 'He said "Python", not "typhoon"' to encode a (double) quote.
6. Boolean values are the two constant objects True and False used to represent truth values (in numeric contexts 1 is True, while 0 is False.


Extra  
There is one more, special literal that is used in Python: the None literal. This literal is a NoneType object, and it is used to represent the absence of a value.





2 Operators
Key takeaways
1. An expression is a combination of values (or variables, operators, calls to functions ‒ you will learn about them soon) which evaluates to a certain value, e.g., 1 + 2.
2. Operators are special symbols or keywords which are able to operate on the values and perform (mathematical) operations, e.g., the * operator multiplies two values: x * y.
3. Arithmetic operators in Python: + (addition), - (subtraction), * (multiplication), / (classic division ‒ always returns a float), % (modulus ‒ divides left operand by right operand and returns the remainder of the operation, e.g., 5 % 2 = 1), ** (exponentiation ‒ left operand raised to the power of right operand, e.g., 2 ** 3 = 2 * 2 * 2 = 8), // (floor/integer division ‒ returns a number resulting from division, but rounded down to the nearest whole number, e.g., 3 // 2.0 = 1.0)
4. A unary operator is an operator with only one operand, e.g., -1, or +3.
5. A binary operator is an operator with two operands, e.g., 4 + 5, or 12 % 5.
6. Some operators act before others - the hierarchy of priorities:
the ** operator (exponentiation) has the highest priority;
then the unary + and - (note: a unary operator to the right of the exponentiation operator binds more strongly, for example 4 ** -1 equals 0.25)
then: *, /, and %,
and finally, the lowest priority: binary + and -.
7. Subexpressions in parentheses are always calculated first, e.g., 15 - 1 * (5 * (1 + 2)) = 0.
8. The exponentiation operator uses right-sided binding, e.g., 2 ** 2 ** 3 = 256.





2
Variables
Here is a short story:
Once upon a time in Appleland, John had three apples, Mary had five apples, and Adam had six apples. They were all very happy and lived for a long time. End of story.
Your task is to:
create the variables: john, mary, and adam;
assign values to the variables. The values must be equal to the numbers of fruit possessed by John, Mary, and Adam respectively;
having stored the numbers in the variables, print the variables on one line, and separate each of them with a comma;
now create a new variable named total_apples equal to the addition of the three previous variables.
print the value stored in total_apples to the console;
experiment with your code: create new variables, assign different values to them, and perform various arithmetic operations on them (e.g., +, -, *, /, //, etc.). Try to print a string and an integer together on one line, e.g., "Total number of apples:" and total_apples.








3
Loops 
1. There are two types of loops in Python: while and for:
the while loop executes a statement or a set of statements as long as a specified boolean condition is true, e.g.:


# Example 1
while True:
    print("Stuck in an infinite loop.")
 
# Example 2
counter = 5
while counter > 2:
    print(counter)
    counter -= 1
 
the for loop executes a set of statements many times; it's used to iterate over a sequence (e.g., a list, a dictionary, a tuple, or a set – you will learn about them soon) or other iterable objects (e.g., strings). You can use the for loop to iterate over a sequence of numbers using the built-in range function. Look at the examples below:


# Example 1
word = "Python"
for letter in word:
    print(letter, end="*")
 
# Example 2
for i in range(1, 10):
    if i % 2 == 0:
        print(i)
 
2. You can use the break and continue statements to change the flow of a loop:
You use break to exit a loop, e.g.:
text = "OpenEDG Python Institute"
for letter in text:
    if letter == "P":
        break
    print(letter, end="")
 
You use continue to skip the current iteration, and continue with the next iteration, e.g.:


text = "pyxpyxpyx
for letter in text:
    if letter == "x":
        continue
    print(letter, end="")
 
3. The while and for loops can also have an else clause in Python. The else clause executes after the loop finishes its execution as long as it has not been terminated by break, e.g.:


n = 0
 
while n != 3:
    print(n)
    n += 1
else:
    print(n, "else")
 
print()
 
for i in range(0, 3):
    print(i)
else:
    print(i, "else")
 
4. The range() function generates a sequence of numbers. It accepts integers and returns range objects. The syntax of range() looks as follows: range(start, stop, step), where:
start is an optional parameter specifying the starting number of the sequence (0 by default)
stop is an optional parameter specifying the end of the sequence generated (it is not included),
and step is an optional parameter specifying the difference between the numbers in the sequence (1 by default.)
Example code:
for i in range(3):
    print(i, end=" ")  # Outputs: 0 1 2
 
for i in range(6, 1, -2):
    print(i, end=" ")  # Outputs: 6, 4, 2
 


---------------------------------------------------------
--------------------------------------------------------


print("ha halee lu yah,..")  
print("The itsy bitsy spider climbed up the waterspout.")
print("Down came the rain and washed the spider out.")
print("The itsy bitsy spider\nclimbed up the waterspout.")
print()
print("Down came the rain\nand washed the spider out.")

print("The itsy bitsy spider\\nclimbed up the waterspout.")
print()
print("Down came the rain\\nand washed the spider out.")
print()
print("The itsy bitsy spider" , "climbed up" , "the waterspout.")
print("My name is", "Python.")
print("Monty Python.")

print()
print("My name is", "Python.", end=" ")
print("Monty Python.")

print()
print("My name is", "Python.", end="")
print("Monty Python.")

print()
print("My", "name", "is", "Monty", "Python.", sep="-")

print()
print("with end below 2 code lines print in one line..")
print("My", "name", "is", sep="_", end="*")
print("Monty", "Python.", sep="*", end="*\n")

print()
print("Programming","Essentials","in", sep="*",end="...")
print("Python")


print("        *        "*2)
print("       * *       "*2)
print("      *   *      "*2)
print("     *     *     "*2)
print("    *       *    "*2)
print("   *         *   "*2)
print("  *           *  "*2)
print(" *             * "*2)
print("******     ******"*2)
print("     *     *     "*2)
print("     *     *     "*2)
print("     *     *     "*2)
print("     *     *     "*2)
print("     *     *     "*2)
print("     *     *     "*2)
print("     *******     "*2)


print(0o123)
print(0x123)


print(4)
print(4.0)
print(3E8)
print()
print(0.0000000000000000000001)

print(True > False)
print(True < False)


print(2+2)
print(2 ** 3)
print(2 ** 3.)
print(2. ** 3)
print(2. ** 3.)

print()
print(6 / 3)
print(6 / 3.)
print(6. / 3)
print(6. / 3.)
print(6 // 4)
print(6. // 4)


print(-6 // 4)
print(6. // -4)

"""


"""
a = 6
b = 3
a /= 2 * b
print(a)
print()
print()

print(14 % 4)
print(2 ** 3)
print(8 ** 2)
print(2 ** 3 ** 2)
print(64 * 64)
print()
print(5 % 13)
print(2 * 13)
print( ( (25 % 13) + 100) / (2 * 13)   )
print((5 * ((25 % 13) + 100) / (2 * 13)) // 2)

"""

"""
print("Tell me anything...")
anything = input()
print("Hmm...", anything, "... Really?")


anything = float(input("Enter a number: "))
something = anything ** 2.0
print(anything, "to the power of 2 is", something)

"""

"""
print("+" + 10 * "-" + "+")
print(("|" + " " * 10 + "|\n") * 5, end="")
print("+" + 10 * "-" + "+")
"""

"""

print()
x = int(input("enter input parameters"))

print(   1 /  ( x + (1 / (x + (1 / (x+ (1/x)))) )) )

print()
x = int(input("enter input parameters"))

print(   1 /  ( x + (1 / (x + (1 / (x+ (1/x)))) )) )

print()
x = int(input("enter input parameters"))

print(   1 /  ( x + (1 / (x + (1 / (x+ (1/x)))) )) )



print()
x = int(input("enter input parameters"))

print(   1 /  ( x + (1 / (x + (1 / (x+ (1/x)))) )) )


"""


"""
hour = int(input("Starting time (hours): "))
mins = int(input("Starting time (minutes): "))
dura = int(input("Event duration (minutes): "))
mins = mins + dura # find a total of all minutes
print("mins")
print(mins)
print(mins // 60)
hour = hour + mins // 60 # find a number of hours hidden in minutes and update the hour
print("hours")
print(hour)
mins = mins % 60 # correct minutes to fall in the (0..59) range
print("mins")
print(mins)
hour = hour % 24 # correct hours to fall in the (0..23) range
print("hours")
print(hour)
print(hour, ":", mins, sep='')

"""


"""
print (1/1)

x = int(input())
y = int(input())
 
x = x % y
x = x % y
y = y % x
 
print(y)

"""

"""

x = 1 / 2 + 3 // 3 + 4 ** 2
print(x)

n = int(input("Enter a number: "))
print(n >= 100)

"""


"""

# Read three numbers
number1 = int(input("Enter the first number: "))
number2 = int(input("Enter the second number: "))
number3 = int(input("Enter the third number: "))
 
# We temporarily assume that the first number
# is the largest one.
# We will verify this soon.
largest_number = number1
 
# We check if the second number is larger than the current largest_number
# and update the largest_number if needed.
if number2 > largest_number:
    largest_number = number2
 
# We check if the third number is larger than the current largest_number
# and update the largest_number if needed.
if number3 > largest_number:
    largest_number = number3
 
# Print the result
print("The largest number is:", largest_number)

"""

"""
# Read three numbers.
number1 = int(input("Enter the first number: "))
number2 = int(input("Enter the second number: "))
number3 = int(input("Enter the third number: "))
 
# Check which one of the numbers is the greatest
# and pass it to the largest_number variable.
 
largest_number = max(number1, number2, number3)
 
# Print the result.
print("The largest number is:", largest_number)

"""

"""
income = float(input("Enter the annual income: "))

if income < 85528:
	tax = income * 0.18 - 556.02
else:
	tax = (income - 85528) * 0.32 + 14839.02

if tax < 0.0:
	tax = 0.0

tax = round(tax, 0)
print("The tax is:", tax, "thalers")


for i in range(10):
    print("The value of i is currently", i)


counter = 5
while counter != 0:
    print('Inside the loop.', counter)
    counter -= 1
print('Outside the loop.', counter)

import time
i=1

    # Write a for loop that counts to five.
    # Body of the loop - print the loop iteration number and the word "Mississippi".
    # Body of the loop - use: time.sleep(1)
    
for i in range(5):
    print(i, "Mississippi")
    time.sleep(1)

print("Ready or not, here I come!")

my_list = [10, 1, 8, 3, 5]
total = 0
 
for i in my_list:
    total += i
 
print(total)

"""

"""
















