# PRG101-Lab3
### Submission Details

In this lab, you will create nine simple scripts. Write the scripts in GitHub codespaces. 
Please note that you must complete the lab during class hours and show your progress to the professor (unless otherwise instructed) to receive the marks for the lab.
Also carefully read the lab submission instructions given at the end of this file.

### Lab Objectives
- To be able to use while loop and for loop
- To be able to use break and continue statements
- To be able to use data type List.

Loops are used in all programming languages for multiple situations. Loops use an expression and will repeat the code under the expression until the expression is True. In investigation 4 you will learn about the 2 types of loops; `while loop` and `for loop`.

## INVESTIGATION 1: USING  while LOOP
In Python, a while loop is used to execute a block of statements repeatedly until a given condition/expression is satisfied. When the condition becomes false, the line immediately after the loop in the program is executed. while loops may use the same type of expression/condition found in IF statements. While the expression is evaluated to True, the code - indented under the while loop will be repeated. When the expression becomes False the loop will stop repeating the indented - code.
All the statements are indented by the same number of character spaces after a programming construct are considered to be part of a single block of code.

```
while expression:
    statement(s)

```
- A while loop is used commonly in scenarios where you would like to repeat certain statements until an event is True or False. While loop is also called event-controlled loop. Below is a WHILE loop which will run five times. Each time the loop is run, it will add one to the variable `count`, increasing the value of the `count`. The variable `count` is iteration variable and it values changes in each iteration.
  
  ``` Python
  count = 0  # iteration variable, while loop requires a relevant variable which is used in the loop expression
  while count != 5: # expression (evaluates to True or False)
      print(count)   # Loop body
      count = count + 1  # Loop body, count is incremented,  or else the loop will continue forever
  print('loop has ended')  # This statement is not part of loop body. This statement will be executed once the loop condition becomes false.
  ```
  ### lab3a.py
- Fill in required fields in comment section
- Copy the above code block in lab4a.py.
- Change the value of count to 1 and then run the program to see how many times the loop runs.
- Next change the while condition to `count < 5 ` and then run the program to see how many times the loop runs.
- Next change the condition to `count <= 5` and then run the program to see how many times the loop runs.
- What did you observe in all of the above examples when you change the value of loop variable or the expression. It is important that you are well aware of initial value of loop variable and the condition in the loop expression to know exactly how many times the loop will be executed.
- Search on internet about "What is off by 1 error in loops"?
- No need to take a screenshot for lab3a. This task does not need to be submitted.

Next we will do a more complex but really useful example.
In python, we often use `while loop` to see if the user entered the required value. We keep asking the user for a value until the user enters the correct value. This is a scenario driven by an event rather than driven by a counter, because you do not know how many times the user will enter the incorrect value before they type in the correct value. See the example below:

```Python
guess = 5
number = int(input("Guess what number less than 10 I am thinking of?"))
while number != guess:  # loop condition 
  print("incorrect guess, try again...")
  number = int(input("Guess what number less than 10 I am thinking of?")) # keep taking input from user until the user enters the correct guess.
print("You got it right!") # this statement will be executed when loop has terminated which will only happen when the user enters the number 5.

```
Now attempt the following task which is based on this previous example.

### lab3b.py
- Fill in required fields in the comments section.
- The script should include a variable `pin`.
- The value of `pin` should be a 4 digit code entered by the user.
- Use a while loop to create a program that won't end until the user enters the correct pin 1234.
- The result should be like this:
```
Please type in your PIN: 0000
Incorrect...try again

Please type in your PIN: 199

Incorrect...try again

Please type in your PIN: 1234
Correct PIN, You can enter!
```
Keep practicing, attempt this next exercise now!

### lab3c.py
The `while True` loop in Python is used when you need to create a loop that runs indefinitely until a specific condition is met. It’s a powerful tool when you need continuous execution until an external event or condition explicitly stops the loop, like a `break` statement or an `exit` condition within the loop body.
The following tasks requires to handle the user input, check for invalid numbers, process correct numbers, and exit the loop when zero is entered.
- Write a `while True` loop.
- Inside the loop body add statements to perform the following actions:
    - Ask the user to enter a number ( use input function, and, then use int() to convert the user input to an integer number).
    - Use if-elif-else statements to check:
        - If the user inputs a negative number, the program prints "Invalid number." and prompts for a new input. Use `continue` statement.
        - If the user inputs zero, the program prints "Exiting..." and terminates. Use break statement.
        - For any other non-negative number; the program calculates the square root of the number and prints the square root as output.
    - The program continues to prompt the user for input until the user enters zero.
- The result should be: 
``` Python

Please type in a number: 9
3.0

Please type in a number: 1
1.0

Please type in a number: -9
Invalid number.

Please type in a number: 0
Exiting ...
```
## INVESTIGATION 2: USING  for LOOP
A `for loop` is used for iterating over a sequence (that could be either a list, a tuple, a dictionary, a set, or a string).
With the `for loo`p we can execute a set of statements, once for each item in a list, tuple, set etc.
A very common example of `for loop` found in all text books is:

``` Python
fruits = ["apple", "banana", "cherry", "date"]

# Use a for loop to iterate over the list
for fruit in fruits:
    print(fruit)
```
`for loop` is commonly used with `range()` function. The `range()` function in Python produces a sequence of integers based on the parameters provided and is commonly used with `for loops`. Here's another example using the `range()` function to print numbers from 0  to 5.

``` Python
for i in range(5):
    print(i)
```
The `range(5)` function generates a sequence of numbers from 0 to 4 (inclusive of 0, exclusive of 5).


### lab3d.py
Write a Python program that calculates the sum of all even numbers from 1 to 100 (inclusive).
- Use a for loop to iterate over the range of numbers from 1 to 100.
- Inside the loop, check if the current number is even.
- If the number is even, add it to a running total.
- After the loop, print the final sum.

### lab3e.py
Write a program that prints the multiplication table of a number taken from user as input using a `for loop`.
Print the multiplication table of` the number` from 1 to 10.

If the user enters the number 5 as input then the output should be like this:
``` Python
5 X 1 = 5
5 X 2 = 10
...
5 X 10 = 50
```

  
## INVESTIGATION 3: USING LISTS

A list in Python is an ordered collection of items that can be of different types. Lists are mutable, meaning you can change their content after creation.
In this Part you will be creating lists and performing basic operations on lists using list methods and built-in functions.
Lists are used to store data elements. Usually lists contain similar kind of data, but python does not restrict you from adding values of different data types in a list.

### lab3f.py
### Creating lists and list concatenation
Lists are constructed with brackets [] and commas separating every element in the list. For example:
```Python
numbers=[1,2,3,4]
mixed_list=[1, "two", 4.5, True]
```
- Fill in the required fields in the comment section
- Create a variable of the type list called `mylist1` and save first three odd numbers (1,3,5) in it.
- Create a second variable of the type list and call it `mylist2`, save first three even numbers (0,2,4) in it.
- Create a third variable called `mylist`. This variable should contain all elements form mylist1 and mylist2. Remember you can use + to concatenate lists, just like we did for strings.
- Print the variable `mylist`.

### lab3g.py
### Using list methods to add and remove elements from a list 

- Fill in the required fields in the comment section.
- Create a variable `mylist` that conatins  first 6 natural numbers.
- Use the `append()` method and add a new element, number 7 in the variable `mylis`t. 
- Use the `inser()` method and insert the element 0 at index 0.
- Use the `pop()' method to remove the element from index 2.
- Print the variable `mylist`.
- Add another statement in the script to find the index of the element 6 and print `The element 6 is present at the index ---`

## lab3h.py
### Modifying a list and using the list in a loop
- Fill in the required fields in the comment section.
- Create a list variable called `students`. Add the following names in this list: Ama, Elina, Maija, Daniel, Ibrahim.
- Next change the element at index 1 and update this element with "Maggy".
- Now use a` for loop` and iterate over this list and print each element on a separate line. 

  
## lab3i.py
### Two Dimensional Lists
A great feature of of Python data structures is that they support *nesting*. This means we can have data structures within data structures. For example: A list inside a list.
A 2D list is a list where each element is itself a list. These inner lists represent rows, and the elements within them represent columns.

```Python
matrix = [
[1, 2, 3],
[4, 5, 6],
[7, 8, 9]
]

element = matrix[1][2]  # Output: 6
```
- Fill in the required fields in the comment section.
- Copy the above code in the file `lab3i.py`.
- Print the element `5` from this list. Specify the correct row and column.
- Print the element `2` from this list.
- Print the element `9` from this list.
- Use a for loop and print individual lists from this matrix. You need a single for loop. The output should be like this:
  ```python
  [1,2,3]
  [4,5,6]
  [7,8,9]
  ```


## Lab 3 Sign-Off
- Submit the screenshots of each individual script, the screenshot must show your scripts and command line interface and output.
- The screenshot must also show your username on github codespaces.
- Make sure screenshots are not blurry, they should be easily readable.
- Please do not leave empty lines in your code, so that your script can fit in one screen.
- Submit individual screenshots of the following scripts on blackboard. If the screenshots do not correctly show the information mentioned above, you will need to re-do and resubmit lab with late penalty in effect.
    - lab3b.py
    - lab3c.py
    - lab3d.py
    - lab3e.py
    - lab3f.py
    - lab3g.py
    - lab3h.py
    - lab3i.py
