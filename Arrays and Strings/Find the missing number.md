# Find the Missing Number

1. [Problem Statement](#problem-statement)
2. [Solution via Arithmetic](#solution-via-arithmetic)
3. [Solution via Python](#solution-via-python)


### Problem Statement

Given an array ```nums``` containing ```n``` distinct numbers in the range ```[0, n]```, return the only number in the range that is missing from the array. 

### Solution via Arithmetic

Consider the array ```nums``` containing ```n = 3``` distinct numbers in the range ```[0, 3]```. To determine if a number is missing from ```nums```, say 2, we can think in terms of the sum of the entries. In other words, 

$$0 + 1 + 3 = 0 + 1 + (2 - 2) + 3 = (0 + 1 + 2 + 3) - 2.$$

Re-arranging the sum and solving for 2 yields

$$(0 + 1 + 2 + 3) - (0 + 1 + 3) = 2,$$

where the sum on the left involves the entries of the complete range ```[0, n]``` and the sum on the right involves the entries of the incomplete range with one number removed. The general case follows immediately. Let $m$ be the missing number. Then, for an arbitrary chosen missing number $m$ may be determined using the equation

$$m = (0 + 1 + 2 + \dots + n) - ((0 + 1 + 2 + \dots + n) - m),$$

where $m = 0, 1, 2, \dots, n$. 

### Solution via Python 

```python
def missingNumber(self, nums: List[int]) -> int: 
  return sum(list(range(len(nums))) - sum(nums) 
```














