# [717. 1-bit and 2-bit Characters](https://leetcode.com/problems/1-bit-and-2-bit-characters/description/)

## 2018/4/16 beats 95.78 % of python3
### Spend 40 ms
```python
class Solution:
    def isOneBitCharacter(self, bits):
        """
        :type bits: List[int]
        :rtype: bool
        """
        if bits == [0]:
            return True
        else:
            bits1 = bits[-2::-1] + [0]
            return sum(bits1[:bits1.index(0)])%2 == 0

```
