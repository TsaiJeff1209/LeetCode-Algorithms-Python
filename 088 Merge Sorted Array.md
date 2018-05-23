# [88. Merge Sorted Array](https://leetcode.com/problems/merge-sorted-array/description/)

## 2018/5/23 beats 100.00 % of python3
### Spend 36 ms
```python
class Solution:
    def merge(self, nums1, m, nums2, n):
        """
        :type nums1: List[int]
        :type m: int
        :type nums2: List[int]
        :type n: int
        :rtype: void Do not return anything, modify nums1 in-place instead.
        """
        nums1[m:m+n] = nums2
        nums1.sort()
```
