# Single Number

## 2018/3/27 beats 95.72 % of python3
### Spend 44 ms
```python
class Solution:
    def singleNumber(self, nums):
        """
        :type nums: List[int]
        :rtype: int
        """
        return sum(set(nums))*2 - sum(nums)
```
