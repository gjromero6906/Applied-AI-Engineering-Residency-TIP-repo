# Day 2

for i in range(len(nums)):
for j in range(i+1,len(nums)):
if nums[i] +nums[j] == target:
return [i,j]
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
