# [67. Add Binary](https://leetcode.com/problems/add-binary/description/)

## 2018/3/29 beats 99.89 % of python3
### Spend 40 ms
```python
class Solution:
    def addBinary(self, a, b):
        """
        :type a: str
        :type b: str
        :rtype: str
        """
        return bin(int(a,2)+int(b,2))[2:]
```
