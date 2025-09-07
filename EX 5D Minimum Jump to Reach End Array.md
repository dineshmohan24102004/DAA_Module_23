# EX 5D Minimum Jump to Reach End Array

## AIM:
To design a Python program that finds the minimum number of jumps required to reach the end of an array, where each element in the array represents the maximum number of steps that can be jumped forward from that index.


## Algorithm
Start the program.

Input the size n of the array.

Read n integers into the array arr[].

Define recursive function minJumps(arr, l, h) that:

Returns 0 if l == h (already at the end).

Returns ∞ (infinity) if arr[l] == 0 (cannot move forward).

Otherwise, initializes min = ∞.

Iterates through all reachable indices from l to l + arr[l].

Recursively calculates jumps from each index.

Updates min with the smallest number of jumps found.

Returns min.

Call minJumps(arr, 0, n-1) to compute the answer.

Print the minimum number of jumps required.

Stop the program.  

## Program:
```
/*
To implement the program to finding the minimum number of jumps needed to reach end of the array.


Developed by: Dinesh M
Register Number: 212222040039

def minJumps(arr, l, h):
    ###########   Add your code here ###########
    if (h == l):
        return 0
    if (arr[l] == 0):
        return float('inf')
    min = float('inf')
    for i in range(l + 1, h + 1):
        if (i < l + arr[l] + 1):
            jumps = minJumps(arr, i, h)
            if (jumps != float('inf') and
                       jumps + 1 < min):
                min = jumps + 1
    return min
arr = []
n = int(input()) 
for i in range(n):
    arr.append(int(input()))
print('Minimum number of jumps to reach','end is', minJumps(arr, 0, n-1))
 
*/
```

## Output:
<img width="1251" height="699" alt="Screenshot 2025-09-07 191102" src="https://github.com/user-attachments/assets/75f6a1da-1fd9-4b04-82f6-1a2fdaec0c03" />



## Result:
The program successfully computes and prints the minimum number of jumps needed to reach the last index.
