# EX 5A Minimum Cost Path

## AIM:
To write a Python program that finds the minimum cost path in a cost matrix from the top-left corner (0,0) to a target cell (m,n) using dynamic programming.




## Algorithm
Start the program.

Input the number of rows R and columns C.

Define a 2D array cost representing the cost matrix.

Define a function minCost(cost, m, n) that:

Creates a temporary table tc[R][C] to store the minimum costs.

Initialize tc[0][0] = cost[0][0].

Print the result.

Stop the program.

## Program:
```
/*
A program to implement to find the Minimum Cost Path Problem using a  Naive recursive Approach.

Developed by: Dinesh M
Register Number: 212222040039
R = int(input())
C = int(input())
def minCost(cost, m, n):
    tc = [[0 for x in range(C)] for x in range(R)]
    tc[0][0] = cost[0][0]
    for i in range(1, m+1):
        tc[i][0] = tc[i-1][0] + cost[i][0]
    for j in range(1, n+1):
        tc[0][j] = tc[0][j-1] + cost[0][j]
    for i in range(1, m+1):
        for j in range(1, n+1):
            tc[i][j] = min(tc[i-1][j-1], tc[i-1][j], tc[i][j-1]) + cost[i][j]
 
    return tc[m][n]
 
cost = [[1, 2, 3],
        [4, 8, 2],
        [1, 5, 3]]
print(minCost(cost, R-1, C-1))
*/
```

## Output:
<img width="1274" height="325" alt="Screenshot 2025-09-07 190404" src="https://github.com/user-attachments/assets/5cfcbbbe-7fe8-469b-aea4-7c9b15ebd18e" />



## Result:
The program was successfully executed.
It calculates and prints the minimum cost required to travel from the starting cell (0,0) to the destination cell (R-1, C-1) by moving only right, down, or diagonally.
