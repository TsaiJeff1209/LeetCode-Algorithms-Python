# [520. Detect Capital](https://leetcode.com/problems/detect-capital/description/)

## 2018/3/25 beats 95.89 % of python3
### Spend 48 ms
```python
class Solution:
    def detectCapitalUse(self, word):
        """
        :type word: str
        :rtype: bool
        """
        if word.upper() == word:
            return True
        elif word.lower() == word:
            return True
        elif word.capitalize() == word:
            return True
        else:
            return False
```
