# Reverse Integer

## 2018/3/24 beats 95.87 % of python3
### Spend 56 ms
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
            return 0
```


