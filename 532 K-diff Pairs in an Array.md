# [532. K-diff Pairs in an Array](https://leetcode.com/problems/k-diff-pairs-in-an-array/description/)

## 2018/4/12 beats 100.00 % of python3
### Spend 48 ms
```python
class Solution:
    def findPairs(self, nums, k):
        """
        :type nums: List[int]
        :type k: int
        :rtype: int
        """
        if k < 0:
            return 0
        elif k == 0:
            return len(set([i for i in nums if nums.count(i)>1]))
        else:
            nums1 = list(set(nums))
            x = [i-k for i in nums1] + nums1
            return len(x)-len(set(x))
```
