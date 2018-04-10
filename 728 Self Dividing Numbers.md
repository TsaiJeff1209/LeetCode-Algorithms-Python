# [728. Self Dividing Numbers](https://leetcode.com/problems/self-dividing-numbers/description/)

## 2018/3/27 beats 69.34 % of python3
### Spend 76 ms
```python
class Solution:
    def selfDividingNumbers(self, left, right):
        """
        :type left: int
        :type right: int
        :rtype: List[int]
        """
        my_list = []
        for i in range(left,right+1):
            j = str(i)    
            if '0' not in j:
                if sum([i % int(x) for x in j]) == 0:
                    my_list.append(i)
        return my_list
```


