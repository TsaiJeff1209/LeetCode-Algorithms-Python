# [70. Climbing Stairs](https://leetcode.com/problems/climbing-stairs/description/)

## [Fibonacci number](https://en.wikipedia.org/wiki/Fibonacci_number)
## 2018/5/10 beats 100.00 % of python3
### Spend 32 ms
```python
class Solution:
    def climbStairs(self, n):
        """
        :type n: int
        :rtype: int
        """
        return  round((1/5**0.5)*(0.5*(1+5**0.5))**(n+1))
```
