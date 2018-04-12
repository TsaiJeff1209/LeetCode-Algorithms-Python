# [766. Toeplitz Matrix](https://leetcode.com/problems/toeplitz-matrix/description/)

## 2018/4/12 beats 91.43 % of python3
### Spend 56 ms
```python
class Solution:
    def isToeplitzMatrix(self, matrix):
        """
        :type matrix: List[List[int]]
        :rtype: bool
        """
        if len(matrix)==1 or len(matrix[0])==1:
            return True
    
        my_list = []
        for i in matrix:
            my_list += i
        if len(set(my_list)) > len(matrix)+len(matrix[0])-1:
            return False

        n = len(matrix)
        start = n-1
        while start >= 0:
            i = start
            my_list = []
            for j in range(min(n-i,len(matrix[0]))):
                my_list.append(matrix[i][j])
                i += 1
            if len(set(my_list)) != 1:
                return False
            start -= 1
    
        n = len(matrix[0])
        start = n-1
        while start > 0:
            i = start
            my_list = []
            for j in range(min(n-i,len(matrix))):
                my_list.append(matrix[j][i])
                i += 1
            if len(set(my_list)) != 1:
                return False
            start -= 1

        return True
```

## 2018/4/12 beats 91.43 % of python3
### Spend 56 ms
### 參照別人做法
```python
class Solution:
    def isToeplitzMatrix(self, matrix):
        """
        :type matrix: List[List[int]]
        :rtype: bool
        """
        if len(matrix)==1 or len(matrix[0])==1:
            return True
        prev_row = matrix[0][:-1]
        for row in matrix[1:]:
            if row[1:] != prev_row:
                return False
            prev_row = row[:-1]
        return True
```
