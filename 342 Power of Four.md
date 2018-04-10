# [342. Power of Four](https://leetcode.com/problems/power-of-four/description/)

## 2018/3/28 beats 95.15 % of python3
### Spend 56 ms
```python
class Solution:
    def isPowerOfFour(self, num):
        """
        :type num: int
        :rtype: bool
        """
        if num <= 0:
            return False
        elif num%10==2 or num%10==8:
            return False
        return 2147483648 % num ==0
```
