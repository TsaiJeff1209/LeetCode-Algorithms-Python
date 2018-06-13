# [387. First Unique Character in a String](https://leetcode.com/problems/first-unique-character-in-a-string/description/)

## 2018/3/25 beats 86.46 % of python3
### Spend 88 ms
```python
class Solution:
    def firstUniqChar(self, s):
        """
        :type s: str
        :rtype: int
        """
        if len(s) == 0:
            return -1
        s1 = s
        while len(s1) > 0:
            if s1.count(s1[0]) == 1:
                return s.find(s1[0])
            s1 = s1.replace(s1[0],"")
        return -1
```
---
## 2018/6/13 beats 87.74 % of python3
### Spend 72 ms
```python
class Solution:
    def firstUniqChar(self, s):
        """
        :type s: str
        :rtype: int
        """
        n = len(s)
        s1 = s
        while n > 0:
            s2 = s1[0]
            s1 = s1.replace(s2,'')
            if n-len(s1)==1:
                return s.find(s2)
            n = len(s1)
        return -1
```
