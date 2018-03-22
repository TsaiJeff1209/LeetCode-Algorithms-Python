# Two Sum
```python
class Solution:
    def twoSum(self, nums, target):
        """
        :type nums: List[int]
        :type target: int
        :rtype: List[int]
        """
        my_nums = [i + abs(min(nums)) for i in nums]
        my_target = target + 2*abs(min(nums))

        if len([i for i in my_nums if i == my_target/2]) == 2:
            return [i for i in range(len(nums)) if target/2 == nums[i]]
        elif len([i for i in my_nums if i == my_target/2]) > 0:
            my_nums = [i for i in my_nums if i != my_target/2]
        
        my_nums = [ i for i in my_nums if i <= my_target]
        nega_nums = [my_target - i for i in my_nums]
        return [nums.index(i-abs(min(nums))) for i in my_nums if i in nega_nums]     
```
