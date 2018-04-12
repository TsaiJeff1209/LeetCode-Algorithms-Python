# [263. Ugly Number](https://leetcode.com/submissions/detail/149672695/)

## 2018/4/12 beats 93.94 % of python3
### Spend 56 ms
```python
class Solution:
    def isUgly(self, num):
        """
        :type num: int
        :rtype: bool
        """
        if num < 1:
            return False
        while num % 2 ==0:
            num //= 2
        while num % 3 ==0:
            num //= 3
        while num % 5 ==0:
            num //= 5
        return num == 1

```
