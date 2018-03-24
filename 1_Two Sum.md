# Two Sum

## 2018/3/21 Your runtime beats 21.42 % of python3 submissions.
### Spend 6876 ms
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

## 2018/3/22 Your runtime beats 22.84 % of python3 submissions.
### Spend 4332 ms
```python
class Solution:
    def twoSum(self, nums, target):
        """
        :type nums: List[int]
        :type target: int
        :rtype: List[int]
        """
        if len(nums) == 2:
            return [0,1]
        if nums.count(target/2) == 2:
            n = nums.index(target/2)
            return [n, nums.index(target/2,n+1)]
    
        my_nums = [i for i in nums if nums.count(i) == 1]
    
        if nums.count(target/2) == 1:
            my_nums.remove(target/2)

        if min(nums) < 0:
            my_target = target + 2*abs(min(my_nums))
            my_nums = [i + abs(min(my_nums)) for i in my_nums if i + abs(min(my_nums)) <= my_target]
            nega_nums = [my_target - i for i in my_nums]
            temp = [*my_nums,*nega_nums]
            n = max(temp, key = temp.count) - abs(min(nums))
        else:
            my_target = target
            my_nums = [ i for i in my_nums if i <= my_target]
            nega_nums = [my_target - i for i in my_nums]
            temp = [*my_nums,*nega_nums]
            n = max(temp, key = temp.count)
        
        return [nums.index(n), nums.index(target-n)]
```

## 2018/3/23 Your runtime beats 57.23 % of python3 submissions.
### Spend 64 ms
```python
class Solution:
    def twoSum(self, nums, target):
        """
        :type nums: List[int]
        :type target: int
        :rtype: List[int]
        """
        dic = {}
        for i, num in enumerate(nums):
            rem = target - num
            if rem in dic:
                return [dic[rem], i]
            dic[num] = i
        return None
```
第一次玩LeetCode發現可以參照神手的答案,因此參考解答答出來的，從4332ms降到64ms，非常佩服神人們的邏輯和運算速度，同時我嘗試了使用list和dict兩種作法，沒想到差異可以這麼大，如下：
* List spend 596 ms , beats 37.22 %
* Dict spend  64 ms , beats 57.32 %  

Google Dict特性：
1：查找速度快　2：浪費空間　3：key不可以重複，且不可變　4：資料無序排放



