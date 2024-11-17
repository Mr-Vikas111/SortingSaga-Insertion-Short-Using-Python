# SortingSaga-Insertion-Short-Using-Python

Insertion sort is a sorting algorithm that places an unsorted element at its suitable place in each iteration.
Insertion sort works similarly as we sort cards in our hand in a card game.
We assume that the first card is already sorted then, we select an unsorted card. If the unsorted card is greater than the card in hand, it is placed on the right otherwise, to the left. In the same way, other unsorted cards are taken and put in their right place.
A similar approach is used by insertion sort.

```
def insertionSort(arr):
    arr_len =len(arr)
    for i in range(1,arr_len):
        current =arr[i]
        prev = i - 1
        while prev >= 0 and current < arr[prev]:
            arr[prev+1] = arr[prev]
            prev -= 1
        arr[prev+1] = current
    return arr

arr = [9, 5, 1, 4, 3]

# call function
insertionSort(arr) -> return -> [1, 3, 4, 5, 9]

```


# Practice Questions (Basic)

1. Trace the insertion sort algorithm for the array:
Input: [8, 4, 6, 2, 9, 1]
Output: Show the array at each step.

```
def InsertionSortStep(arr):
    arr_len = len(arr)
    for i in range(1,arr_len):
        curr = arr[i]
        prev = i - 1
        while prev >= 0 and curr < arr[prev]:
            arr[prev+1] = arr[prev]
            prev -= 1
        
        arr[prev+1] = curr
        print(f"Step {i}: {arr}")
    return arr

arr = [8, 4, 6, 2, 9, 1]

# call function
InsertionSortStep(arr)
```
Output:
```
Step 1: [4, 8, 6, 2, 9, 1]
Step 2: [4, 6, 8, 2, 9, 1]
Step 3: [2, 4, 6, 8, 9, 1]
Step 4: [2, 4, 6, 8, 9, 1]
Step 5: [1, 2, 4, 6, 8, 9]
sorted_array [1, 2, 4, 6, 8, 9]
```


