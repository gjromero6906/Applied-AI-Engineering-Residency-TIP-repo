```py
class Solution(object):
    def maxSubArray(self, nums):
        """
        :type nums: List[int]
        :rtype: int
        """
        current_sum = max_sum = nums[0]

        for num in nums[1:]:
            current_sum = max(num, current_sum + num)
            max_sum = max(max_sum, current_sum)

        return max_sum
```

Tool Best For
Counter Counting frequencies of elements
`defaultdict(list)` Grouping items into lists
`defaultdict(set)` Grouping unique items
`defaultdict(int)` Building custom frequency maps

A good rule of thumb:

If you're counting things, reach for Counter.
If you're constantly writing if key not in dictionary:, reach for defaultdict.
collections.Counter

`Counter` is a specialized dictionary from Python's collections module that automatically counts how many times each item appears in a list, string, or other iterable. Instead of creating an empty dictionary and manually checking whether a key already exists before increasing its count, `Counter` does all of that work in a single line. It stores each unique item as a key and the number of times it appears as the value. This makes it especially useful for problems involving frequency counting, such as finding the most common element, checking if two strings are anagrams, or solving "Top K Frequent Elements" style interview questions. To use it, import it with from collections import `Counter` and create a `counter` by passing in an iterable, such as `Counter(nums)`.

`collections.defaultdict`

`defaultdict` is a dictionary-like data structure from Python's collections module that automatically provides a default value when you access a key that does not yet exist. In a normal dictionary, trying to use a missing key would raise a KeyError, so programmers often have to write extra code to check whether a key exists before adding values to it. A `defaultdict` removes this boilerplate by creating the default value for you automatically. For example, `defaultdict(list)` creates an empty list whenever a new key is accessed, making it perfect for grouping items, while `defaultdict(int)` starts missing keys at 0, making counting easier. This feature helps keep code cleaner, shorter, and easier to read, especially when working with collections of grouped or counted data.
