# Day 3

```py
left = 0
right = len(s)-1
while left < right:
    temp = s[left]
    s[left] = s[right]
    s[right] = temp
    left = left +1
    right = right -1
return s
```

This code snippet reverses a list or array `s` in place by swapping the elements at the `left` and `right` indices until the entire sequence is reversed.

```py
class Solution(object):
    def lengthOfLongestSubstring(self, s):
        """
        :type s: str
        :rtype: int
        """
        seen = {}
        left = 0
        max_length = 0

        for right, char in enumerate(s):
            if char in seen and seen[char] >= left:
                left = seen[char] + 1

            seen[char] = right
            max_length = max(max_length, right - left + 1)

        return max_length
```

The `lengthOfLongestSubstring` method finds the longest substring without repeating characters by sliding a window across the string and using a dictionary to remember the most recent index of each character. When a repeated character is found, it moves the start of the window forward to keep the substring unique.
