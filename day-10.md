```py
class Solution(object):
    def frequencySort(self, s):
        """
        :type s: str
        :rtype: str
        """
        from collections import Counter

        counts = Counter(s)
        result = ""

        for char, count in counts.most_common():
            result += char * count
        return result
```
