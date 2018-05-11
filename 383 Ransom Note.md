# [383. Ransom Note](https://leetcode.com/problems/ransom-note/description/)

## 2018/5/11 beats 100.00 % of python3
### Spend 40 ms
```python
class Solution:
    def canConstruct(self, ransomNote, magazine):
        """
        :type ransomNote: str
        :type magazine: str
        :rtype: bool
        """
        for i in set(ransomNote):
            if ransomNote.count(i) > magazine.count(i):
                return False
        return True

```
