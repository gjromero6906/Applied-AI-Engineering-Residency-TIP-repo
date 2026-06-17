```py
class Solution(object):
    def longestConsecutive(self, nums):
        """
        :type nums: List[int]
        :rtype: int
        """
        if not nums:
            return 0
        newNums = set(nums)
        length = len(nums)
        count = 0
        hold = 1
        for x in newNums:
            if x + 1 not in newNums:
                count = max(count,hold)
            else:
                hold += 1
        return count
```
