# [747. Largest Number At Least Twice of Others](https://leetcode.com/problems/largest-number-at-least-twice-of-others/description/)

## 2018/4/12 beats 99.11 % of python3
### Spend 40 ms
```python
class Solution:
    def dominantIndex(self, nums):
        """
        :type nums: List[int]
        :rtype: int
        """
        m1 = max(nums)
        i = nums.index(m1)
        nums = [i for i in nums if i>0]
        if len(nums)==1:
            return i
        nums.remove(m1)
        m2 = max(nums)
        if m1/m2 >= 2:
            return i
        else:
            return -1
```

經修正，將 ```if m1/m2 >= 2:``` 修改成 ```if m1 >= 2*m2```
可以省去 ```nums = [i for i in nums if i>0]``` 
### 因為可以避免到分母為0的狀況，因此之後有需要條件判斷時，可考量變數不放分母的等式

```python
class Solution:
    def dominantIndex(self, nums):
        """
        :type nums: List[int]
        :rtype: int
        """
        m1 = max(nums)
        i = nums.index(m1)
        if len(nums)==1:
            return i
        nums.remove(m1)
        m2 = max(nums)
        if m1 >= 2*m2:
            return i
        else:
            return -1
```
