# Queue-Remove Two String Values from the Rear End in Python 🧵

This Python program demonstrates how to manage a list of strings and remove the last two elements (i.e., from the rear of the list).

## 🎯 Aim

To write a Python program to:
- Accept `n` string values from the user
- Remove the last two values (rear end of the list)
- Display the updated list

## 🧠 Algorithm

1. Create an empty list `q`.
2. Read an integer `n` from the user (number of strings).
3. Loop `n` times:
   - Read a string input.
   - Append it to the list `q`.
4. Remove the last element using `pop()`.
5. Remove the next last element using `pop()` again.
6. Display the updated list.

##  Program:
```
q = []
n = int(input("Enter the number of strings: "))

for _ in range(n):
    val = input("Enter a string: ")
    q.append(val)

q.pop()
q.pop()

print("Updated list:", q)
```

### Output:
![image](https://github.com/user-attachments/assets/8a4101b8-f1b0-4404-9e16-2cd65a8c48ae)

## Result:
Thus,the program is executed successfully
