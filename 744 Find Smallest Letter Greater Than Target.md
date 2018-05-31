# [744. Find Smallest Letter Greater Than Target](https://leetcode.com/problems/find-smallest-letter-greater-than-target/description/)

## 2018/5/31 beats 100.00 % of python3
### Spend 40 ms
```python
class Solution:
    def nextGreatestLetter(self, letters, target):
        """
        :type letters: List[str]
        :type target: str
        :rtype: str
        """
        if letters[-1] <= target:
            return letters[0]
        else:
            l = sorted(list(set(letters)))
            for i in l:
                if i>target: return i
```
