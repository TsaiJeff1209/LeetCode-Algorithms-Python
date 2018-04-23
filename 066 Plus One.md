# [66. Plus One](https://leetcode.com/problems/plus-one/description/)

## 2018/4/24 beats 95.20 % of python3
### Spend 40 ms
```python
class Solution:
    def plusOne(self, digits):
        """
        :type digits: List[int]
        :rtype: List[int]
        """
        return [int(i) for i in str(int("".join(map(str,digits)))+1)]
        
```
