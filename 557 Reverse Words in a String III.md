# [557. Reverse Words in a String III](https://leetcode.com/problems/reverse-words-in-a-string-iii/description/)

## 2018/4/3 beats 96.96 % of python3
### Spend 40 ms ( both versions have same performance )
```python
class Solution:
    def reverseWords(self, s):
        """
        :type s: str
        :rtype: str
        """
        return " ".join(s[::-1].split(" ")[::-1])
```
