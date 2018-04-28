# [541. Reverse String II](https://leetcode.com/problems/reverse-string-ii/description/)

## 2018/4/28 beats 99.69 % of python3
### Spend 36 ms
```python
class Solution:
    def reverseStr(self, s, k):
        """
        :type s: str
        :type k: int
        :rtype: str
        """
        s1 = [s[i:i+k] for i in range(0,len(s),k)]
        return ''.join([x[::-1] if i%2==0 else x for i,x in enumerate(s1)])
```
