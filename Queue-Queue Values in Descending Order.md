# Queue-Queue Values in Descending Order Using Python 🧮

This Python program simulates a queue using a list, removes the first two elements (FIFO order), and displays the remaining values in descending order.

## 🎯 Aim

To write a Python program to:
- Accept user inputs into a list (queue)
- Remove the first two elements (simulating dequeue)
- Display the remaining values in **descending order**

## 🧠 Algorithm

1. Create an empty list `q`.
2. Read an integer `n` to determine how many elements will be added.
3. Loop `n` times:
   - Read an input value.
   - Append it to the list `q`.
4. Remove the first element using `pop(0)`.
5. Remove the second element using `pop(0)` again.
6. Sort the list in descending order.
7. Print the updated list.

## 🧪 Program: 
```
def words_to_number(word):
    word_map = {
        "one": 1, "two": 2, "three": 3, "four": 4, "five": 5,
        "six": 6, "seven": 7, "eight": 8, "nine": 9, "ten": 10
    }
    return word_map.get(word.lower(), None)

q = []
n = int(input("Enter the number of elements to add to the queue: "))

print(f"Enter {n} values (e.g., one, two, three):")
for _ in range(n):
    word = input()
    number = words_to_number(word)
    if number is not None:
        q.append(number)
    else:
        print(f"Invalid input: {word}. Please enter a valid word between one and ten.")

if len(q) >= 2:
    q.pop(0)
    q.pop(0)

q.sort(reverse=True)
print("Updated list in descending order:", q)
```
### Output:
![image](https://github.com/user-attachments/assets/ef49d77f-6971-48ef-be12-af167dc683f9)

## Result:
Thus,the program is executed successfully
