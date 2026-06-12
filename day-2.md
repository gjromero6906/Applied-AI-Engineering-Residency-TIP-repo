# Day 2

```py
for i in range(len(nums)):
    for j in range(i+1,len(nums)):
        if nums[i] +nums[j] == target:
            return [i,j]

This nested loop version checks every pair of numbers in `nums` and returns the first pair of indices whose values add up to the `target`.

class Solution(object):
    def maxProfit(self, prices):
    """
    :type prices: List[int]
    :rtype: int
    """
    minPrice = float('inf')
    maxProfit = 0
    for price in prices:
        if price <minPrice:
            minPrice = price
        elif price - minPrice > maxProfit:
            maxProfit = price - minPrice
    return maxProfit
```

The `maxProfit` method finds the largest profit from a single stock buy-and-sell by tracking the lowest price seen so far and updating the maximum profit whenever a higher difference is found.
