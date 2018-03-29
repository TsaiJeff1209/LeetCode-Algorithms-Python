# Hamming Distance

## 2018/3/30 beats 93.20 % of python3
### Spend 40 ms
```python
class Solution:
    def hammingDistance(self, x, y):
        """
        :type x: int
        :type y: int
        :rtype: int
        """
        a = bin(x)[2:].zfill(32)
        b = bin(y)[2:].zfill(32)
        return sum([1 for i in range(32) if a[i]!=b[i]])
```

## 2018/3/30 beats 93.20 % of python3
### Spend 40 ms
```python
class Solution:
    def hammingDistance(self, x, y):
        """
        :type x: int
        :type y: int
        :rtype: int
        """
        return len(format(x ^ y, 'b').replace('0',""))
```
## 2018/3/30 beats 98.95 % of python3
### Spend 36 ms
```python
class Solution:
    def hammingDistance(self, x, y):
        """
        :type x: int
        :type y: int
        :rtype: int
        """
        return format(x ^ y, 'b').count('1')
```
