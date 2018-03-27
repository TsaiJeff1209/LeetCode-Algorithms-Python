# Power of Three

## 2018/3/27 beats 80.00 % of python3
### Spend 468  ms
### 作者指定不要用迴圈或遞迴的作法
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
網友的解答想法很特別，把n當做分母，分子放3的19次方(恰好小於2的31次方)，沒有參照網友做法的話，很容易陷入迴圈思維。
