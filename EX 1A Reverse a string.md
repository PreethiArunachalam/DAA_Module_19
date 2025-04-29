# EX 1A Factorial of a Number
## DATE: 18/02/25
## AIM:
To write a program to print the factorial of a number recursively.

## Algorithm
1. Define a function fact(n) to calculate the factorial
2. Read an integer input n
3. If n is 0, return 1
4. Else, recursively multiply n by the factorial of n-1
5. Display the result as the factorial of the number

## Program:
```
/*
Program to implement Reverse a String
Developed by: Preethi A A
Register Number: 212222110035
*/
```
```
def fact(n):
    if n==0:
        return 1
    else:
        return n*fact(n-1)
n=int(input())
print("Factorial of number",n,"=",fact(n))
```

## Output:

![image](https://github.com/user-attachments/assets/efe2a4fc-fa45-43cb-99e4-07c68892d56a)

## Result:
The program successfully displays the factorial of the number. When the user provides an input number, the output displays the factorial of that number
