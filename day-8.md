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
        for x in newNums:
            if x-1 not in newNums:
                currentNum = x
                hold = 1
                while currentNum + 1 in newNums:
                    currentNum += 1
                    hold +=1
                count = max(count,hold)

        return count
```
