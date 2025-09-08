# Experiment-5
# Name:RAGAVAN M
# Register Number:212224230216
## AIM:Write a python program for Binary Search and inspect for failures. 

# ALGORITHM
1.Start the program.

2. Get the list from the user

3. Get the element to be searched

4. Compare the mid element with the key, if same return the index

5. If key is greater, search it in the right side, else search it in the left side.

6. If not found return -1

7. Stop the program. 

 # PROGRAM
```
def is_sorted(arr):
    return all(arr[i] <= arr[i+1] for i in range(len(arr)-1))

def binary_search(arr, key):
    low, high = 0, len(arr) - 1
    while low <= high:
        mid = (low + high) // 2
        if arr[mid] == key:
            return mid
        elif key > arr[mid]:
            low = mid + 1
        else:
            high = mid - 1
    return -1


arr = list(map(int, input("Enter list elements: ").split()))
key = int(input("Enter element to search: "))


if not is_sorted(arr):
    print("Failure: Binary Search requires a sorted array. The given array is not sorted.")
else:
    result = binary_search(arr, key)
    if result != -1:
        print(f"Element found at index {result}")
    else:
        print("Element not found")

```

 # OUTPUT
 <img width="877" height="80" alt="image" src="https://github.com/user-attachments/assets/c6430d52-8424-430f-993a-825f8b5b3c1c" />

 <img width="927" height="89" alt="image" src="https://github.com/user-attachments/assets/351bb546-d307-4a86-8d28-3eef27ab1637" />

# RESULT
Thus,the Python program for Binary Search was successfully executed and failures were inspected.
