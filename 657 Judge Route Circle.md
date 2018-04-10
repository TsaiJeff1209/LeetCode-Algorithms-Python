# [657. Judge Route Circle](https://leetcode.com/problems/judge-route-circle/description/)

## 2018/4/3 beats 98.96 % of python3
### Spend 40 ms
```python
class Solution:
    def judgeCircle(self, moves):
        """
        :type moves: str
        :rtype: bool
        """
        return (moves.count("R") == moves.count("L")) & (moves.count("U") == moves.count("D"))
```
