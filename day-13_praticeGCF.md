```py
class Solution(object):
    def runningSum(self, nums):
        """
        :type nums: List[int]
        :rtype: List[int]
        """
        totals = []
        total = 0

        for i in nums:
            total = total + i
            totals.append(total)
        return totals

```

```py
class Solution(object):
    def maxVowels(self, s, k):
        """
        :type s: str
        :type k: int
        :rtype: int
        """
        vowels = set("aeiou")

        # Count vowels in the first window
        count = 0
        for i in range(k):
            if s[i] in vowels:
                count += 1

        maximum = count

        # Slide the window
        for i in range(k, len(s)):
            if s[i] in vowels:
                count += 1

            if s[i - k] in vowels:
                count -= 1

            maximum = max(maximum, count)

        return maximum
```
