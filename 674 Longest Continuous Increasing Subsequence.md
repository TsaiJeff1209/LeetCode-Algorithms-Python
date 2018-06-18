# [674. Longest Continuous Increasing Subsequence](https://leetcode.com/problems/longest-continuous-increasing-subsequence/description/)

## 2018/6/18 beats 98.30 % of python3
### Spend 44 ms
```python
class Solution:
    def findLengthOfLCIS(self, nums):
        """
        :type nums: List[int]
        :rtype: int
        """
        if len(nums) <= 1: return len(nums)
        n,m = 1,1
        for i in range(len(nums)-1):
            if nums[i+1] > nums[i]:
                n += 1
            else:
                n = 1
            if n > m:
                m = n
        return m

```
