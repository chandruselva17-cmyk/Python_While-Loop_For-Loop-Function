# Python_While-Loop_For-Loop-Function
Assignment covering iteration, control flow and functions in Python, built around three practical programs: a number guessing game, a multiplication table generator and a BMI calculator.

Objectives

Iteration using while and for loops

Control statements: break, continue, pass and the loop else clause

Defining and calling functions

Applying these to real-world style problems

Contents

File	Task	Concepts used

task1_guessing_game.py	Number guessing game	while loop, continue, break, while...else, random.randint()

task2_multiplication_table.py	Multiplication table generator	for loop, range(), f-strings

task3_bmi_calculator.py	BMI calculator	Function definition, return, numeric formatting

Task 1 — Number Guessing Game

The program generates a random number between 1 and 10 and gives the user three attempts to guess it.

Guesses outside 1–10 are rejected with a message and continue sends control back to the top of the loop, without using up an attempt.

A correct guess prints a congratulation and exits the loop with break.

The else block attached to the while loop runs only if the loop ends without break, i.e. when the user runs out of attempts.

Sample output

Guess the number (between 1 and 10): 2
Too low. Try again.

Guess the number (between 1 and 10): 15
Your guess is out of range. Please guess a number between 1 and 10.

Guess the number (between 1 and 10): 5
Too high. Try again.

Guess the number (between 1 and 10): 3
Congratulations! You guessed the correct number.

Task 2 — Multiplication Table Generator

The user enters a number and the program prints its multiplication table from 1 to 10 using a for loop over range(1, 11).

Sample output

Enter the number for which you want the multiplication table: 5
5 x 1 = 5
5 x 2 = 10
5 x 3 = 15
5 x 4 = 20
5 x 5 = 25
5 x 6 = 30
5 x 7 = 35
5 x 8 = 40
5 x 9 = 45
5 x 10 = 50

Task 3 — BMI Calculator

A calculate_bmi(weight, height) function returns the Body Mass Index using the formula:

BMI = weight (kg) / height (m) ** 2

The main program collects the weight and height from the user, calls the function and prints the result rounded to two decimal places.

Sample output
Enter your weight in kg: 58

Enter your height in meters: 1.62

Your BMI is: 22.10

Notes and possible improvements

Input is converted directly with int() and float(), so non-numeric input will raise a ValueError. Wrapping the conversions in try / except would make the programs more robust.

In Task 1, invalid guesses deliberately do not consume an attempt. Moving the attempts -= 1 line above the range check would change this behaviour.
