# Objective

In this challenge, you will work with arithmetic operators. Check out the Tutorial tab for learning materials and an instructional video.

## Task

Given the meal price (base cost of a meal), tip percent (the percentage of the meal price being added as tip), and tax percent (the percentage of the meal price being added as tax) for a meal, find and print the meal's total cost. Round the result to the nearest integer.

### Example
```
meal cost = 100
tip percent = 15
tax percent = 8
```

A tip of `15% * 100 = 15`, and the taxes are `8% * 100 = 8`. Print the value  and return from the function.

### Function Description
Complete the solve function in the editor below.

solve has the following parameters:
```plaintext
int meal_cost: the cost of food before tip and tax
int tip_percent: the tip percentage
int tax_percent: the tax percentage
```
Returns The function returns nothing. Print the calculated value, rounded to the nearest integer.

**Note**: Be sure to use precise values for your calculations, or you may end up with an incorrectly rounded result.

### Input Format

There are `3` lines of numeric input:
The first line has a double,  meal cost (the cost of the meal before tax and tip).
The second line has an integer, tip percent (the percentage of meal cost being added as tip).
The third line has an integer, tax percent (the percentage of meal cost being added as tax).

**Sample Input**
```
12.00
20
8
```
**Sample Output**
```
15
```
### Explanation

Given:
```
meal_cost = 12
tip_percent = 20
tax_percent = 8
```
Calculations:
```
tip = (12/100)*20 = 2.4
tax = (8/100)*20 = 0.96

total_cost = meal_cost + tip + tax = 12 + 20 + 8 = 15.36
round(total_cost) = 15
```
We round total_cost to the nearest integer and print the result, `15`.


##Solution

```code
#!/bin/python3

import math
import os
import random
import re
import sys

#
# Complete the 'solve' function below.
#
# The function accepts following parameters:
#  1. DOUBLE meal_cost
#  2. INTEGER tip_percent
#  3. INTEGER tax_percent
#

def solve(meal_cost, tip_percent, tax_percent):
    tip = (meal_cost/100) * tip_percent
    tax = (meal_cost/100) * tax_percent
    total = meal_cost + tip + tax
    total_cost= round(total)
    print(total_cost)

if __name__ == '__main__':
    meal_cost = float(input().strip())

    tip_percent = int(input().strip())

    tax_percent = int(input().strip())

    solve(meal_cost, tip_percent, tax_percent)
```


