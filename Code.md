# Bubble Sort

```
def bubble_sort_optimized(arr):
    n = len(arr)
    for i in range(n):
        swapped = False
        for j in range(0, n-i-1):
            if arr[j] > arr[j+1]:
                arr[j], arr[j+1] = arr[j+1], arr[j]
                swapped = True
        if not swapped:
            break
    return arr
```

# Quick Sort

```
def median_of_three(arr, low, high):
    mid = (low + high) // 2
    if arr[low] > arr[mid]:
        arr[low], arr[mid] = arr[mid], arr[low]
    if arr[low] > arr[high]:
        arr[low], arr[high] = arr[high], arr[low]
    if arr[mid] > arr[high]:
        arr[mid], arr[high] = arr[high], arr[mid]
    arr[mid], arr[high] = arr[high], arr[mid]
    return arr[high]

def quick_sort_optimized(arr, low, high):
    if low < high:
        pivot = median_of_three(arr, low, high)
        pi = partition(arr, low, high)
        quick_sort_optimized(arr, low, pi-1)
        quick_sort_optimized(arr, pi+1, high)
    return arr
```
