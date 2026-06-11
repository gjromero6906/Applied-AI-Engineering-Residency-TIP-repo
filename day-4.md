# Day 4

```py
class Solution(object):
    def containsDuplicate(self, nums):
    """
    :type nums: List[int]
    :rtype: bool
    """
    seen = set()
    for i in range(len(nums)):
        if nums[i] in seen:
            return True
        seen.add(nums[i])
    return False

class Solution(object):
    def groupAnagrams(self, strs):
        """
        :type strs: List[str]
        :rtype: List[List[str]]
        """
        hold = {}
        for i in range(len(strs)):
            key = ''.join(sorted(strs[i]))
            if key not in hold:
                hold[key] = []
            hold[key].append(strs[i])
        return list(hold.values())
```
