# 🔄 Types of Queue-Circular Queue in Python

This project demonstrates the implementation of a **Circular Queue** in Python. The queue accepts 3 user values, performs enqueue and dequeue operations, and displays the removed values.

---

## 🎯 Aim

To develop a Python program that implements a Circular Queue:
- Accepts 3 values from the user
- Removes the 3 values from the queue
- Displays the removed values

---

## 🧠 Algorithm

1. **Initialize** a circular queue of fixed size (e.g., 5).
2. **Define the following functions**:
   - `enqueue()`: Inserts an element into the queue.
   - `dequeue()`: Removes an element from the queue.
   - `display()`: Shows the queue contents.
3. Accept 3 values from the user using the `enqueue()` method.
4. Remove 3 values using the `dequeue()` method.
5. Print the removed values.

---

## 💻 Program:
```
class CircularQueue:
    def __init__(self, size):
        self.size = size
        self.queue = [None] * size
        self.front = self.rear = -1

    def enqueue(self, value):
        if (self.rear + 1) % self.size == self.front:
            print("Queue is full.")
            return
        if self.front == -1:
            self.front = 0
        self.rear = (self.rear + 1) % self.size
        self.queue[self.rear] = value

    def dequeue(self):
        if self.front == -1:
            print("Queue is empty.")
            return None
        removed = self.queue[self.front]
        if self.front == self.rear:
            self.front = self.rear = -1
        else:
            self.front = (self.front + 1) % self.size
        return removed

    def display(self):
        if self.front == -1:
            print("Queue is empty.")
            return
        i = self.front
        print("Queue contents:", end=" ")
        while True:
            print(self.queue[i], end=" ")
            if i == self.rear:
                break
            i = (i + 1) % self.size
        print()


cq = CircularQueue(5)

for i in range(3):
    val = input(f"Enter value {i+1}: ")
    cq.enqueue(val)

removed_values = []
for _ in range(3):
    removed = cq.dequeue()
    if removed is not None:
        removed_values.append(removed)

print("Removed values:", removed_values)
```
### Output:
![image](https://github.com/user-attachments/assets/a6c0b7d6-b688-4cce-b851-1c63febb2e35)

## Result:
Thus,the program is executed successfully
