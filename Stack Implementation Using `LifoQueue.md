# Stack Implementation Using `LifoQueue` (Max Size 7) 🔄

This Python program demonstrates a stack implemented using the `LifoQueue` class from the `queue` module. It allows up to 7 elements, checks if the stack is full, and then prints the elements in reverse (LIFO) order.

## 🎯 Aim

To create a Python program that:
- Implements a stack using `LifoQueue` with a maximum size of 7
- Adds user-inputted values to the stack
- Checks whether the stack is full
- Prints the stack elements in reverse order (LIFO)

## 📋 Algorithm

1. Import the `LifoQueue` class from the `queue` module.
2. Create a stack with a maximum size of 7.
3. Read the number of elements (`n`) to be added to the stack.
4. Loop `n` times:
   - Read a value from the user.
   - Use `put()` to push it onto the stack if it's not full.
5. Use `full()` to check if the stack is full and print the result.
6. Use `get()` repeatedly to pop and print elements in reverse order.

## Program
```
from queue import LifoQueue

stack = LifoQueue(maxsize=7)
n = int(input("Enter the number of elements to push (max 7): "))

for _ in range(n):
    if not stack.full():
        val = int(input("Enter a value: "))
        stack.put(val)
    else:
        print("Stack is full. Cannot add more elements.")
        break

print("Is the stack full?", stack.full())

print("Stack elements in LIFO order:")
while not stack.empty():
    print(stack.get())
```

## 🧪 Sample Input and Output
![image](https://github.com/user-attachments/assets/48b99133-957e-482b-b0f6-7d7e03b33566)

## Result:
Thus,the program is executed successfully
