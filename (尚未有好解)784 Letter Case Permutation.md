# Letter Case Permutation

## 2018/4/7 beats 71.22 % of python3
### Spend 80 ms
```python
class Solution:
    def letterCasePermutation(self, S):
        """
        :type S: str
        :rtype: List[str]
        """
        S = S.lower()
        my_set = set([S])
        for i in range(len(S)):
            if S[i].isalpha():
                for j in list(my_set):
                    my_set.add(j[:i]+S[i].lower()+S[i+1:])
                    my_set.add(j[:i]+S[i].upper()+S[i+1:])
        return list(my_set)

```
