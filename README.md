# Simple Calculator
import math

print("CALCULATOR")
print("Select operation:")
print("a. Addition")
print("b. Subtraction")
print("c. Multiplication")
print("d. Division")
print("e. Floor Division")
print("f. Modulus")
print("g. Exponent")
print("h. Logarithm")

# Get user choice
choice = input("Enter your choice and watch the magic happen (a-h): ").lower()

if choice in ['a', 'b', 'c', 'd', 'e', 'f', 'g']:
    print("One more step left: ")
    num1 = float(input("Enter first number: "))
    num2 = float(input("Enter second number: "))

    if choice == 'a':
        print(f"Voila: {num1 + num2}")
    elif choice == 'b':
        print(f"Voila: {num1 - num2}")
    elif choice == 'c':
        print(f"Voila: {num1 * num2}")
    elif choice == 'd':
        if num2 != 0:
            print(f"Voila: {num1 / num2}")
        else:
            print("Error: Division by zero is not allowed.")
    elif choice == 'e':
        if num2 != 0:
            print(f"Voila: {num1 // num2}")
        else:
            print("Error: Division by zero is not allowed.")
    elif choice == 'f':
        if num2 != 0:
            print(f"Voila: {num1 % num2}")
        else:
            print("Error: Modulus by zero is not allowed.")
    elif choice == 'g':
        print(f"Voila: {num1 ** num2}")

# Logarithm (only one input)
elif choice == 'h':
    num = float(input("Enter a positive number: "))
    base = input("Enter base: ")
    
    if num <= 0:
        print("Error: Dude..... srsly?")
    else:
        if base == "":
            print(f"Voila: {math.log(num)}")  
        else:
            base = float(base)
            if base <= 0 or base == 1:
                print("Error:Gosh.")
            else:
                print(f"Voila: {math.log(num, base)}")

else:
    print("C'man bro, just this once make the right choice.")
 
