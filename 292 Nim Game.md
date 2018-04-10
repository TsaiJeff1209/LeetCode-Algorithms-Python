# [292. Nim Game](https://leetcode.com/problems/nim-game/)

## 2018/3/26 beats 100.00 % of python3
### Spend 32 ms
```python
class Solution:
    def canWinNim(self, n):
        """
        :type n: int
        :rtype: bool
        """
        if n % 4 == 0:
            return False
        else:
            return True
```

## 更聰明的寫法
## 2018/3/26 beats 100.00 % of python3
### Spend 32 ms
```python
class Solution:
    def canWinNim(self, n):
        """
        :type n: int
        :rtype: bool
        """
        return (n%4 != 0)
```
