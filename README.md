# FILE AND EXCEPTION HANDLING

### EXERCISE 1

#### PROGRAM 1

try:
    with open('input.txt', 'r') as file:
        content = file.read()
        print(content)
except FileNotFoundError:
    print("File not found. Please check the filename.")

#### OUTPUT 1    

![image](https://github.com/user-attachments/assets/a85e78bf-9c67-4919-a31f-231124636579)


### EXERCISE 2

#### PROGRAM 2
