# Add Digits

## 2018/4/8 beats 90.75 % of python3
### Spend 60 ms
```python
class Solution:
    def addDigits(self, num):
        """
        :type num: int
        :rtype: int
        """
        while num >= 10:
            n = []
            for i in str(num):
                n.append(int(i))
                num = sum(n)
        return num
```
