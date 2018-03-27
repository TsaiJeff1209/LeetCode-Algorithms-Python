# Power of Three

## 2018/3/27 beats 80.00 % of python3
### Spend 468  ms
```python
class Solution:
    def isPowerOfThree(self, n):
        """
        :type n: int
        :rtype: bool
        """
        if n > 0:
            return 1162261467 % n == 0
        return False
```
作者指定不要用迴圈或遞迴的左法，而網友解答是很特別的想法，把n當做分母，分子放3的19次方(恰好小於2的31次方)，沒有參照別人做法的話，很容易陷入迴圈思維。
