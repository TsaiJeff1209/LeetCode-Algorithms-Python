# Move Zeroes

## 2018/4/8 beats 27.14 % of python3
### Spend 108 ms
```python
class Solution:
    def moveZeroes(self, nums):
        """
        :type nums: List[int]
        :rtype: void Do not return anything, modify nums in-place instead.
        """
        for i in range(nums.count(0)):
            nums.remove(0)
            nums.append(0)
```
