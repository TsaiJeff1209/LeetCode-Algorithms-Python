# Find the Difference

## 2018/3/26 beats 60.18 % of python3
### Spend 52 ms
```python
class Solution:
    def findTheDifference(self, s, t):
        """
        :type s: str
        :type t: str
        :rtype: str
        """
        while len(s) > 0:
            s, t = s.replace(s[0],"",1), t.replace(s[0],"",1)
        return t
```

## 2018/3/26 beats 96.15 % of python3
### Spend 40 ms
```python
class Solution:
    def findTheDifference(self, s, t):
        """
        :type s: str
        :type t: str
        :rtype: str
        """
        for i in range(97,123):
            if s.count(chr(i)) != t.count(chr(i)): return chr(i)
```
