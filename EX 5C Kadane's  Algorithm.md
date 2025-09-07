# EX 5C Kadane's Algorithm

## AIM:
To design a Python program that finds the maximum sum of a contiguous subarray from a given array of integers using Kadane’s Algorithm.


## Algorithm
Start the program.

Input the size n of the array.

Read n integers into the array a[].

Initialize:

max_so_far = a[0] (stores the maximum sum found so far).

max_ending_here = 0 (stores the sum of the current subarray).

Traverse each element of the array:

Add the current element a[i] to max_ending_here.

If max_ending_here < 0, reset it to 0 (discard negative sums).

If max_so_far < max_ending_here, update max_so_far.

After the loop ends, max_so_far contains the maximum contiguous subarray sum.

Print the result.

Stop the program. 

## Program:
```
/*
To implement the program to find the maximum contiguous subarray.


Developed by: Dinesh M
Register Number: 212222040039
def maxSubArraySum(a,size):
    #####################  Add your Code here #############
    max_so_far = a[0]
    max_ending_here = 0
    for i in range(0, size):
        max_ending_here = max_ending_here + a[i]
        if max_ending_here < 0:
            max_ending_here = 0
        elif (max_so_far < max_ending_here):
            max_so_far = max_ending_here
              
    return max_so_far
n=int(input())  
a =[] #[-2, -3, 4, -1, -2, 1, 5, -3]
for i in range(n):
    a.append(int(input()))
print("Maximum contiguous sum is", maxSubArraySum(a,n))
*/
```

## Output:
<img width="1272" height="652" alt="Screenshot 2025-09-07 190855" src="https://github.com/user-attachments/assets/ebc9d5ce-8b59-4dab-8b31-91831b6b2975" />



## Result:
The program successfully computes and prints the maximum contiguous subarray sum.
