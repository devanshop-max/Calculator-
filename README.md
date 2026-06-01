print("=== Advanced Calculator ===")

operations = {
    "+": lambda a, b: a + b,
    "-": lambda a, b: a - b,
    "*": lambda a, b: a * b,
    "/": lambda a, b: a / b,
    "^": lambda a, b: a ** b
}

while True:

    print("\nChoose Operation")
    print("+  Addition")
    print("-  Subtraction")
    print("*  Multiplication")
    print("/  Division")
    print("^  Power")
    print("sqrt  Square Root")
    print("exit  Close Calculator")

    choice = input("Enter operation: ")

    if choice == "exit":
        print("Calculator Closed")
        break

    if choice == "sqrt":
        num = float(input("Enter number: "))
        print("Answer =", math.sqrt(num))
        continue

    num1 = float(input("Enter first number: "))
    num2 = float(input("Enter second number: "))

    result = operations[choice](num1, num2)

    print("Answer =", result)
