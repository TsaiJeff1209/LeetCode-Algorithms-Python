# [268. Missing Number](https://leetcode.com/problems/missing-number/description/)

## 2018/4/10 beats 95.78 % of python3
### Spend 48 ms
```python
class Solution:
    def missingNumber(self, nums):
        """
        :type nums: List[int]
        :rtype: int
        """
        return sum(range(len(nums)+1)) - sum(nums)
```


