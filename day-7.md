```py
class Solution(object):
    def topKFrequent(self, nums, k):
        """
        :type nums: List[int]
        :type k: int
        :rtype: List[int]
        """
        checks = set(nums)
        numOftimes = []
        for num in checks:
            count = 0
            for x in nums:
                if num ==x:
                    count += 1


            numOftimes.append([count,num])
        numOftimes.sort(reverse=True)
        clean=[]
        for i in range(k):
            clean.append(numOftimes[i][1])

        return clean

```
