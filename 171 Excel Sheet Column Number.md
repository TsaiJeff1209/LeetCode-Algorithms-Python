# [171. Excel Sheet Column Number](https://leetcode.com/submissions/detail/155510495/)

## 2018/5/23 beats 99.23 % of python3
### Spend 56 ms
```python
class Solution:
    def titleToNumber(self, s):
        """
        :type s: str
        :rtype: int
        """
        n = 0
        for i,j in enumerate(s[::-1]):
            n += (ord(j)-64) * 26**i
        return n

```
