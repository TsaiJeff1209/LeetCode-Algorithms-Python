# [283. Move Zeroes](https://leetcode.com/problems/move-zeroes/description/)


## 2018/6/1 beats 99.30 % of python3
### Spend 48 ms
### 這樣也算是 modify 呀~ XD
```python
class Solution:
    def moveZeroes(self, nums):
        """
        :type nums: List[int]
        :rtype: void Do not return anything, modify nums in-place instead.
        """
        my_nums = [i for i in nums if i != 0]
        n = len(my_nums)
        nums[:n] = my_nums
        nums[n:] = [0]*(len(nums)-n)
```


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
