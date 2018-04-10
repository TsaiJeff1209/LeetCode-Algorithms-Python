# [771. Jewels and Stones](https://leetcode.com/problems/jewels-and-stones/description/)

## 2018/3/28 beats 93.74 % of python3
### Spend 44 ms
```python
class Solution:
    def numJewelsInStones(self, J, S):
        """
        :type J: str
        :type S: str
        :rtype: int
        """
        n = len(S)
        for i in J:
            S = S.replace(i,"")
        return n - len(S)

```
