# [217. Contains Duplicate](https://leetcode.com/problems/contains-duplicate/description/)

## 2018/3/28 beats 99.51 % of python3
### Spend 44 ms
```python
class Solution:
    def containsDuplicate(self, nums):
        """
        :type nums: List[int]
        :rtype: bool
        """
        if len(nums) <= 1:
            return False
        return len(nums) != len(set(nums))
```
