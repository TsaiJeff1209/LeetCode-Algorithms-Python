# [693. Binary Number with Alternating Bits](https://leetcode.com/problems/binary-number-with-alternating-bits/description/)

## 2018/6/19 beats 100 % of python3
### Spend 36 ms
```python
class Solution:
    def hasAlternatingBits(self, n):
        """
        :type n: int
        :rtype: bool
        """
        s = bin(n)[2:]
        n1 = len(s)
        s = s.replace('11','')
        s = s.replace('00','')
        return len(s)==n1
```
