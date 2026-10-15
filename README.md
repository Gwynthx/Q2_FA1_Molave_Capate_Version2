# Creating a Modular Mini-Program Version 2
def add_numbers(num1, num2):
    return num1 + num2

def subtract_numbers(num1, num2):
    return num1 - num2

def multiply_numbers(num1, num2):
    return num1 * num2

def divide_numbers(num1, num2):
    if num2 == 0:
        return None
    return num1 / num2

def get_number(prompt):
    while True:
        try:
            return float(input(prompt))
        except ValueError:
            print("Please enter a valid number.")

def get_choice():
    print("Choose an operation:")
    print("1) Add")
    print("2) Subtract")
    print("3) Multiply")
    print("4) Divide")
    while True:
        choice = input("Enter 1, 2, 3, or 4: ").strip()
        if choice in ("1", "2", "3", "4"):
            return choice
        print("Invalid choice. Try again.")

def main():
    choice = get_choice()
    num1 = get_number("Enter the first number: ")
    num2 = get_number("Enter the second number: ")

if choice == "1":
        result = add_numbers(num1, num2)
    elif choice == "2":
        result = subtract_numbers(num1, num2)
    elif choice == "3":
        result = multiply_numbers(num1, num2)
    else:
        result = divide_numbers(num1, num2)

 if result is None:
        print("Cannot divide by zero")
    else:
        print("Result:", result)

if __name__ == "__main__":
    main()
