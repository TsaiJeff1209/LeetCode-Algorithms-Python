# [14. Longest Common Prefix](https://leetcode.com/problems/longest-common-prefix/description/)

## 2018/5/23 beats 97.87 % of python3
### Spend 40 ms
```python
class Solution:
    def longestCommonPrefix(self, strs):
        """
        :type strs: List[str]
        :rtype: str
        """
        if strs == []:
            return ""
        elif strs == [""]:
            return "" 
        else:
            i = 1
            n = max([len(i) for i in strs])
            while len(set([s[0:i] for s in strs]))==1 and i<=n:
                i += 1
            return strs[0][0:i-1]
```

## Others, fast solution speed 36 ms
```python
class Solution:
    def longestCommonPrefix(self, strs):
        import os 
        return os.path.commonprefix(strs)
```
