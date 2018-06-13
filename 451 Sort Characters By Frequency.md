# [451. Sort Characters By Frequency](https://leetcode.com/problems/sort-characters-by-frequency/description/)

## 2018/6/13 beats 100.00 % of python3
### Spend 40 ms
```python
class Solution:
    def frequencySort(self, s):
        """
        :type s: str
        :rtype: str
        """
        d = {}
        while len(s) > 0:
            n = s.count(s[0])
            if n in d:
                d[n] = d[n]+s[0]
            else:
                d[n] = s[0]
            s = s.replace(s[0],'')
        for i in sorted(d,reverse=True): s += ''.join([j*i for j in d[i]])
        return s
```
