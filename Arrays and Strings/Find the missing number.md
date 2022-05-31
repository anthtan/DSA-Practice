# Find the Missing Number

### Problem Statement

Given an array ```nums``` containing ```n``` distinct numbers in the range ```[0, n]```, return the only number in the range that is missing from the array. 

### Solution (No Code)

Let us start with a very simple base case, ```n = 3```. Our array ```nums``` has the form $\[0, 1, 2, 3\]$. Consider the difference between the following two sums 

$$(0 + 1 + 2 + 3) - (0 + 1 + 3) = 2.$$

The left sum $(0 + 1 + 2 + 3)$ is the sum from ```0``` to ```n = 3```, while the right sum $0 + 1 + 3$ is missing 2. Notice that by using this difference, we are able to easily spot the missing number. We now generalize for $n > 0$. 

Since the indices are in one-to-one correspondence with the array's data (i.e. ```nums[0] = 0, nums[1] = 1, ...```), we may find the missing number ```nums[j]``` using the equation 

$$(0 + 1 + 2 + \dots + nums\[n\]) - ((0 + 1 + 2 + \dots + nums\[n\]) - nums\[j\]) = nums\[j\], j = 1, \dots, n$$

















