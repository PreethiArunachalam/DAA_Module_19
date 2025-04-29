# EX 1C Quick Sort
## DATE: 25/02/25
## AIM:
To write a python program to implement quick sort using recursion.

## Algorithm
1. Define a function partition() to place the pivot in correct position by rearranging elements
2. Define a function quick_sort() that recursively sorts the array using the partition index
3. Read the number of elements n and take input elements into the list arr
4. Call quick_sort(arr, 0, len(arr)-1) to start sorting the array
5. Print the sorted array arr  

## Program:
```
/*
Program to implement implement quick sort using recursion.
Developed by: Preethi A A
Register Number: 212222110035 
*/
```
```
def partition(arr,low,high):
    pivot=arr[high]
    i=low-1
    for j in range(low,high):
        if arr[j]<=pivot:
            i+=1
            arr[i],arr[j]=arr[j],arr[i]
    arr[i+1],arr[high]=arr[high],arr[i+1]
    return i+1
def quick_sort(arr,low,high):
    if low<high:
        pivot_index=partition(arr,low,high)
        print("pivot: ",arr[pivot_index])
        quick_sort(arr,low,pivot_index-1)
        quick_sort(arr,pivot_index+1,high)
n=int(input())
arr=[]
for i in range(n):
    element=int(input())
    arr.append(element)
quick_sort(arr,0,len(arr)-1)
print(arr)
```

## Output:

![image](https://github.com/user-attachments/assets/93d40482-62e3-481c-8b0a-583ec1236201)

## Result:
The program successfully sorts the input array using the QuickSort algorithm.
