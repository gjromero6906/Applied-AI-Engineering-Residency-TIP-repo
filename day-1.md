# Day 1

```py
class Solution(object):
    def fizzBuzz(self, n):
        """
        :type n: int
        :rtype: List[str]
        """
        result = []

        for i in range(1, n + 1):
            if i % 3 == 0 and i % 5 == 0:
                result.append("FizzBuzz")
            elif i % 3 == 0:
                result.append("Fizz")
            elif i % 5 == 0:
                result.append("Buzz")
            else:
                result.append(str(i))

        return result
```

This `fizzBuzz` method generates a list of strings for the numbers from 1 through `n`, replacing every multiple of 3 with "Fizz", every multiple of 5 with "Buzz", and every multiple of both with "FizzBuzz". It checks each number in turn, appends the correct string to `result`, and returns the completed list.
