# [190. Reverse Bits](https://leetcode.com/problems/reverse-bits/description/)

## 2018/4/28 beats 98.25 % of python3
### Spend 36 ms
```python
class Solution:
    # @param n, an integer
    # @return an integer
    def reverseBits(self, n):
        return int(bin(n)[2:].zfill(32)[::-1],2)
```
