# FILE AND EXCEPTION HANDLING

### EXERCISE 1 (Write a Python program to read a file and display its contents)

#### PROGRAM 1

try:

    with open('input.txt', 'r') as file:
    
        content = file.read()
        
        print(content)
        
except FileNotFoundError:

    print("File not found. Please check the filename.")
    

#### OUTPUT 1    

![image](https://github.com/user-attachments/assets/702850aa-eb11-4554-90b5-1c11717fc14d)



### EXERCISE 2 (Write a Python program to copy the contents of one file to another file)

#### PROGRAM 2

try:

    with open('input.txt', 'r') as source_file, open('output.txt', 'w') as destination_file:
    
        destination_file.write(source_file.read())
        
    print("File copied successfully.")
    
except FileNotFoundError:

    print("File not found. Please check the filename.")
    


#### OUTPUT 2

![image](https://github.com/user-attachments/assets/96a2e6d4-1eb9-4f25-9226-e1e2fa8ad0b7)



### EXERCISE 3 (Write a Python program to read the content of a file and count the total number of words in that file.)

#### PROGRAM 3

try:

    with open('input.txt', 'r') as file:
    
        content = file.read()
        
        words = content.split()
        
        print("Total number of words:", len(words))
        
except FileNotFoundError:

    print("File not found. Please check the filename.")



#### OUTPUT 3

![image](https://github.com/user-attachments/assets/aa5b5b69-8588-486a-a4d9-c8cb8508b96d)



### EXERCISE 4 (Write a Python program that prompts the user to input a string and converts it to an integer. Use try-except blocks to handle any exceptions that might occur)

#### PROGRAM 4

try:

    user_input = input("Enter a string to convert to an integer: ")
    
    number = int(user_input)  # Attempt conversion
    
    print("Converted integer:", number)
    
except ValueError:

    print("Invalid input! The string cannot be converted to an integer.")
    


#### OUTPUT 4

![image](https://github.com/user-attachments/assets/bf2370c0-dfcd-45e2-9238-905bcd2d7ad9)


### Exercise 5 ( Write a Python program that prompts the user to input a list of integers and raises an exception if any of the integers in the list are negative.)

#### PROGRAM 5

try:

    user_list = list(map(int, input("Enter a list of integers separated by spaces: ").split()))
    
    if any(num < 0 for num in user_list):
    
        raise ValueError("Negative numbers are not allowed!")
        
    print("Valid list of numbers:", user_list)
    
except ValueError as e:

    print("Error:", e)
    


#### OUTPUT 5

![image](https://github.com/user-attachments/assets/9977203c-0fe7-4ac9-a294-dd081032f519)


### Exercise 6
#### Write a Python program that prompts the user to input a list of integers and computes the average of those integers. Use try-except blocks to handle any exceptions that might occur.use the finally clause to print a message indicating that the program has finished running.

#### PROGRAM 6

try:

    user_list = list(map(int, input("Enter a list of integers separated by spaces: ").split()))
    
    average = sum(user_list) / len(user_list)
    
    print("Average:", average)
    
except ZeroDivisionError:

    print("Error: Cannot divide by zero (empty list).")
    
except ValueError:

    print("Error: Please enter valid integers.")
    
finally:

    print("Program has finished running.")


  #### OUTPUT 6

  ![image](https://github.com/user-attachments/assets/d63c6b71-a0d2-435a-8fa1-d86dafcbd55a)



### Exercise 7 
#### Write a Python program that prompts the user to input a filename and writes a string to that file. Use try-except blocks to handle any exceptions that might occur and print a welcome message if there is no exception occurred.


#### PROGRAM 7

try:

    filename = input("Enter the filename: ")
    
    with open(filename, 'w') as file:
    
        file.write("Welcome to Python programming!")
        
    print("File written successfully.")
    
except Exception as e:

    print("Error:", e)
    
else:

    print("Welcome! No errors occurred.")


#### OUTPUT 7

![image](https://github.com/user-attachments/assets/7cd7b4cf-73fe-4666-9a46-539875e44748)
