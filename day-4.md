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
```

This `containsDuplicate` method checks if any number appears more than once in `nums` by keeping a set of seen values and returning `True` as soon as a duplicate is encountered.

```
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

The `groupAnagrams` method groups strings that are anagrams of each other by sorting each string to create a canonical key, storing the original strings in a dictionary by that key, and returning the grouped values.
