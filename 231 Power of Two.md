# [231. Power of Two](https://leetcode.com/problems/power-of-two/description/)

## 2018/3/28 beats 95.30 % of python3
### Spend 56 ms
```python
class Solution:
    def isPowerOfTwo(self, n):
        """
        :type n: int
        :rtype: bool
        """
        if n <= 0:
            return False
        return 2147483648 % n == 0
```
