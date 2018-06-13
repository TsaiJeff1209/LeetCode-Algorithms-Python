# [347. Top K Frequent Elements](https://leetcode.com/problems/top-k-frequent-elements/description/)

## 2018/6/13 beats 99.13 % of python3
### Spend 48 ms
```python
from collections import Counter
class Solution:
    def topKFrequent(self, nums, k):
        """
        :type nums: List[int]
        :type k: int
        :rtype: List[int]
        """
        c = Counter(nums)
        return [i for i,j in c.most_common(k)]
```
