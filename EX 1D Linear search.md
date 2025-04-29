# EX 1D Linear search
## DATE: 01/03/25
## AIM:
To write a python program for a search function with parameter list name and the value to be searched using string values.

## Algorithm
1.Read the number of elements and store them in a list List
2.Read the value n to search in the list
3.Loop through each element in List
4.If an element matches n, print "Found" and stop the loop
5.If the loop completes without a match, print "Not Found" 

## Program:
```
/*
Program to implement a search function with parameter list name and the value to be searched using string values.
Developed by: Preethi A A 
Register Number: 212222110035  
*/
```
```
def search(List,n):
    for i in List:
        if i==n:
            print("Found")
            break
    else:
        print("Not Found")
List=[input() for _ in range(int(input()))]
n=input()
```
## Output:

![image](https://github.com/user-attachments/assets/a33517d7-1318-49c5-9f80-8094f22b07b1)


## Result:
The program was executed successfully, and it correctly checks if the input element is present in the list, printing "Found" if the element exists or "Not Found" if it does not.
