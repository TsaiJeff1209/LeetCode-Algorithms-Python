# [747. Largest Number At Least Twice of Others](https://leetcode.com/problems/largest-number-at-least-twice-of-others/description/)

## 2018/4/12 beats 99.11 % of python3
### Spend 40 ms
```python
class Solution:
    def dominantIndex(self, nums):
        """
        :type nums: List[int]
        :rtype: int
        """
        n = max(nums)
        i = nums.index(n)
        nums = [i for i in nums if i>0]
        if len(nums)==1:
            return i
        nums.remove(n)
        m = max(nums)
        if n/m >= 2:
            return i
        else:
            return -1
```
