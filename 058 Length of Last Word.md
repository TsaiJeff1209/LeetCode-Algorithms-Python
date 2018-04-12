# [58. Length of Last Word](https://leetcode.com/problems/length-of-last-word/description/)

## 2018/4/12 beats 96.86 % of python3
### Spend 36 ms
```python
class Solution:
    def lengthOfLastWord(self, s):
        """
        :type s: str
        :rtype: int
        """
        if s.replace(" ","") != "":
            return len([ i for i in s.split(" ") if i != ""][-1])
        else:
            return 0
```
