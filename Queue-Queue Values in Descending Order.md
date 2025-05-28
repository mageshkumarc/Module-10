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
import queue  
q = queue.Queue() 
for i in range(5):
    q.put(input())

n =  q.qsize()  
for i in range(n):  
    x = q.get()  
    for j in range(n-1):  
        y = q.get()  
        if x < y :  
            q.put(y)  
        else:  
            q.put(x)  
            x = y     
    q.put(x)  
while (q.empty() == False):   
    print(q.queue[0], end = " ")    
    q.get()
```
### Output:
![image](https://github.com/user-attachments/assets/2ee4ce91-f0d3-464a-887a-c770377e993d)

## Result:
Thus,the program is executed successfully
