```py
class Solution(object):
    def longestPalindrome(self, s):
        """
        :type s: str
        :rtype: int
        """
        counts = Counter(s)
        length = 0
        has_odd = False

        for count in counts.values():
            if count % 2 == 0:
                length += count
            else:
                length += count - 1
                has_odd = True

        if has_odd:
            length += 1

        return length
```
