# SortingSaga-Insertion-Short-Using-Python

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

insertionSort(arr) -> return -> [1, 3, 4, 5, 9]

```

