# Happy Number

## 2018/3/27 beats 97.07 % of python3
### Spend 48 ms
```python
class Solution:
    def isHappy(self, n):
        """
        :type n: int
        :rtype: bool
        """
        my_list=[]
        while n not in my_list:
            my_list.append(n)
            n = sum([int(i)**2 for i in str(n)])
        return n == 1
```
