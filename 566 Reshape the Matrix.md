# [566. Reshape the Matrix](https://leetcode.com/problems/reshape-the-matrix/description/)

## 2018/3/27 beats 48.28 % of python3
### Spend 148 ms
```python
class Solution:
    def reverse(self, x):
        """
        :type x: int
        :rtype: int
        """
        if x >= 0:
            n = int(str(x)[::-1])
        else:
            n = -int(str(x)[:0:-1])
        if abs(n) < 2**31:
            return n
        else:
           
