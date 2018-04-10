# [496. Next Greater Element I](https://leetcode.com/problems/next-greater-element-i/description/)

## 2018/4/7 beats 27.36 % of python3
### Spend 124 ms
```python
class Solution:
    def nextGreaterElement(self, nums1, nums2):
        """
        :type nums1: List[int]
        :type nums2: List[int]
        :rtype: List[int]
        """
        nums2.append(-1)
        x = []
        for i in nums1:
            nums = nums2[nums2.index(i)+1:]
            if i > max(nums):
                x.append(-1)
            else:
                for j in nums:
                    if j > i:
                        x.append(j)
                        break
        return x
```
