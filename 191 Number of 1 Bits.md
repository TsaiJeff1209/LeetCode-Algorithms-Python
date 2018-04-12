# [191. Number of 1 Bits](https://leetcode.com/problems/number-of-1-bits/description/)

## 2018/4/12 beats 86.05 % of python3
### Spend 37 ms
```python
class Solution(object):
    def hammingWeight(self, n):
        """
        :type n: int
        :rtype: int
        """
        return bin(n)[2:].count("1")
```
