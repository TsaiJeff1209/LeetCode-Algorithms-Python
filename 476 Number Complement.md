# Number Complement

## 2018/4/3 beats 94.27 % of python3
### Spend 40 ms
```python
class Solution:
    def findComplement(self, num):
        """
        :type num: int
        :rtype: int
        """
        # Version. 1
        #return int(''.join('1' if i == '0' else '0' for i in bin(num)[2:]),2)
        
        # Version. 2
        x = bin(num)[2:].replace("1","2")
        x = x.replace("0","1")
        x = x.replace("2","0")
        return int(x,2)

```
