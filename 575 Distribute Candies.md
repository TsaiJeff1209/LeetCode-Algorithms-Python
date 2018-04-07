# Distribute Candies

## 2018/4/8 beats 98.91 % of python3
### Spend 124 ms
```python
class Solution:
    def distributeCandies(self, candies):
        """
        :type candies: List[int]
        :rtype: int
        """
        return min( len(candies)//2 , len(set(candies)) )
```
