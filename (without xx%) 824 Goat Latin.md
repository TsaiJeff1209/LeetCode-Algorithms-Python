# [824. Goat Latin](https://leetcode.com/problems/goat-latin/description/)

## 2018/5/8 beats XX.XX % of python3
### Sorry. We do not have enough accepted submissions to show runtime distribution chart.
### Spend 40 ms
```python
class Solution:
    def toGoatLatin(self, S):
        """
        :type S: str
        :rtype: str
        """
        s = S.split(" ")
        for i,j in enumerate(s):
            if j[0].lower() in ["a","e","i","o","u"]:
                s[i] = j + "ma"
            else:
                s[i] = j[1:] + j[0] + "ma"
            s[i]+= "a" * (i+1)
        return " ".join(s)
```
