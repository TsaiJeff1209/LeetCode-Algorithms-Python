# [35. Search Insert Position](https://leetcode.com/problems/search-insert-position/description/)

## 2018/5/3 beats 99.88 % of python3
### Spend 36 ms
```python
class Solution:
    def searchInsert(self, nums, target):
        """
        :type nums: List[int]
        :type target: int
        :rtype: int
        """
        nums = nums + [target]
        if len(nums) == nums.index(target)+1:
            return sorted(nums).index(target)
        else:
            return nums.index(target)
```

## 第一名跟神一樣
```python
class Solution:
    def searchInsert(self, nums, target):
        num=[i for i in nums if i<target]
        return len(num)
```


