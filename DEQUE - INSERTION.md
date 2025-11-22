# Exp.No:39  
## DEQUE - INSERTION

---

### AIM  
To write a Python program to insert elements at REAR END of deque using a collection built-in function.

---

### ALGORITHM  

1. Import the `deque` class from the `collections` module.  
2. Initialize an empty deque.  
3. Start an infinite loop using `while True`.  
4. In each iteration, take input from the user.  
5. If the input is an empty string, break the loop.  
6. If the input is not empty, convert it to an integer and append it to the deque.  
7. After the loop ends, append the values `14` and `15` to the deque.  
8. Print the message `"The deque after appending at right is :"`.  
9. Print the contents of the deque.  

---

### PROGRAM  

```
import collections
  
n1=input()
n2=input()
n3=input()
# initializing deque
de = collections.deque([n1,n2,n3])

# inserts 14,15 at the end of deque


de.append('h')
de.append('o')
de.append('n')
# printing modified deque
print ("The deque after appending at right is : ")
print (de)
```

### OUTPUT
<img width="1216" height="207" alt="image" src="https://github.com/user-attachments/assets/439a11de-4a16-4ea4-b3a9-8c694281ad83" />


### RESULT
  Thus the program to insert elements at REAR END of deque using a collection built-in function is successfully verified.
