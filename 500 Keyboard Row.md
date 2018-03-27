# Keyboard Row

## 2018/3/27 beats 100.00 % of python3
### Spend 32 ms
```python
class Solution:
    def findWords(self, words):
        """
        :type words: List[str]
        :rtype: List[str]
        """
        s = ["qwertyuiop","asdfghjkla","zxcvbnmzzz"]
        my_list = []
        for i in words:
            n = len(i)
            word1 = i.lower()
            word2 = word1
            word3 = word1
            for j in range(10):
                word1 = word1.replace(s[0][j],"")
                word2 = word2.replace(s[1][j],"")
                word3 = word3.replace(s[2][j],"")
            if ((len(word1)!=n) + (len(word2)!=n) + (len(word3)!=n)) == 1:
                my_list.append(i)
        return my_list
        
```
