# CODSOFT

# Design a simple calculator with basic arithmetic operations. Prompt the user to input two numbers and an operation choice. Perform the calculation and display the result.

  def add(x,y):
    return x+y

def sub(x,y):
    return x-y

def mul(x,y):
    return x*y

def div(x,y):
    return x/y

def calculator():
    print("Select the operation: ")
    print("1. add")
    print("2. sub")
    print("3. mul")
    print("4. div")

while True:
    choice = input("enter your choice (1/2/3/4): ")
    if choice in ('1','2','3','4'):
        try:
            num1 = float(input("enter your first number: "))
            num2 = float(input("enter your second number: "))
        except ValueError:
            print("Invalid input, enter numeric values")
            continue

        if choice == '1':
            print(f"{num1 + num2} = {add(num1,num2)}")
        elif choice == '2':
            print(f"{num1 - num2} = {sub(num1,num2)}")
        elif choice == '3':
            print(f"{num1 * num2} = {mul(num1, num2)}")
        elif choice == '4':
            print(f"{num1 / num2} = {div(num1,num2)}")
        next_calculation = input("Do you want to perform another calculation? (yes/no): ")
        if next_calculation == 'no':
            print("Thank you for using calculator")
            break
