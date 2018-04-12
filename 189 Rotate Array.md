# [189. Rotate Array](https://leetcode.com/problems/rotate-array/description/)

## 2018/4/12 beats 98.75 % of python3
### Spend 52 ms
```python
class Solution:
    def rotate(self, nums, k):
        """
        :type nums: List[int]
        :type k: int
        :rtype: void Do not return anything, modify nums in-place instead.
        """
        n = len(nums)
        nums[:] = nums[n-k:] + nums[:n-k]
#        nums.reverse()
#        for i in range(k):
#            nums.append(nums[0])
#            nums.remove(nums[0])
#        nums.reverse()
```
