# EX 5B Coin Change Problem

## AIM:
To design a Python program that counts the total number of ways to make change for a given amount (target) using a given set of coins (array S).


## Algorithm
Start the program.

Input the number of coin types n.

Input the coin denominations into array S.

Input the target sum (amount) to be made.

Define recursive function count(S, n, target) that:

Returns 1 if target == 0 (a valid combination is found).

Returns 0 if target < 0 (invalid path) or n < 0 (no coins left).

Otherwise, recursively explores two cases:

Include the coin: incl = count(S, n, target - S[n])

Exclude the coin: excl = count(S, n - 1, target)

Return incl + excl as the total number of combinations.

Print the result.

Stop the program. 

## Program:
```
/*
Create a python function to compute the fewest number of coins that we need to make up the amount given.

.
Developed by: Dinesh M
Register Number: 212222040039

def count(S, n, target):
    ###################  Add Your Code Here #################
    if target == 0:
        return 1
    if target < 0 or n < 0:
        return 0
    incl = count(S, n, target - S[n])
    excl = count(S, n - 1, target)
    return incl + excl

if __name__ == '__main__':
    S = []#[1, 2, 3]
    n=int(input())
    target = int(input())
    for i in range(n):
        S.append(int(input()))
    print('The total number of ways to get the desired change is',
        count(S, len(S) - 1, target))
*/
```

## Output:

<img width="1246" height="567" alt="Screenshot 2025-09-07 190642" src="https://github.com/user-attachments/assets/27f25a77-1ef1-4379-bfd3-d3d91a4a75da" />


## Result:
The program successfully computes and prints the total number of ways to make the target amount using the given coins.
