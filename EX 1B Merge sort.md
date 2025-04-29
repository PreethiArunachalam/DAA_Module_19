# EX 1B Merge Sort
## DATE: 22/02/25
## AIM:
To Write a Program for Implementing merge sort using python recursion.

## Algorithm
1. If the array has more than one element, split it into two halves.
2. Recursively apply merge sort on both halves.
3. Compare elements of both halves and merge them into a sorted array.
4. Copy any remaining elements from the left or right half.
5. Return the fully sorted array.  

## Program:
```
/*
Program to implement Merge Sort
Developed by: Preethi A A
Register Number: 212222110035
*/
```
```
def merge_sort(S):
    n = len(S)
    current_size = 1

    while current_size < n:
        left = 0
        while left < n - 1:
            mid = min(left + current_size - 1, n - 1)
            right = min(left + 2 * current_size - 1, n - 1)

            merge(S, left, mid, right)
            left += 2 * current_size

        current_size *= 2


def merge(S, left, mid, right):
    n1 = mid - left + 1
    n2 = right - mid

    L = [S[left + i] for i in range(n1)]
    R = [S[mid + 1 + i] for i in range(n2)]

    i = j = 0
    k = left

    while i < n1 and j < n2:
        if L[i] <= R[j]:
            S[k] = L[i]
            i += 1
        else:
            S[k] = R[j]
            j += 1
        k += 1

    while i < n1:
        S[k] = L[i]
        i += 1
        k += 1

    while j < n2:
        S[k] = R[j]
        j += 1
        k += 1


# Driver code
if __name__ == '__main__':
    # User input for array size
    n = int(input())

    # User input for array elements
    inp_arr = []
    for i in range(n):
        element = int(input())
        inp_arr.append(element)

    print("Input Array:")
    print()
    print(inp_arr)
    merge_sort(inp_arr)
    print("Sorted Array:")
    print()
    print(inp_arr)
```
## Output:

![image](https://github.com/user-attachments/assets/37487f32-236c-416d-b336-db9bef65072e)

## Result:
The program successfully sorts the given array using merge sort. where all the elements in the array has been sorted.
