# [796. Rotate String](https://leetcode.com/problems/rotate-string/description/)

## 2018/3/27 beats 95.95 % of python3
### Spend 36 ms
```python
class Solution:
    def rotateString(self, A, B):
        """
        :type A: str
        :type B: str
        :rtype: bool
        """
        if len(A)+len(B) == 0:
            return True
        for i in range(len(A)):
            if B == A[i+1::]+A[0:i+1]:
                return True
        return False
```
