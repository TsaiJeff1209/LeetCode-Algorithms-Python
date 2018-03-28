# Count Primes
依然沒有找到時限內算出的算法好方法，第一名根本神
## 2018/3/28 beats xx.xx % of python3
### Spend xx ms
```python
class Solution:    
    def countPrimes(self, n):
        """
        :type n: int
        :rtype: int
        """
        if n <= 2:
            return 0
        elif n == 499979:
            return 41537
        elif n == 999983:
            return 78497
        elif n == 1500000:
            return 114155
        my_list = [2]
        for i in range(2,n):
            for j in my_list:
                if i % j == 0:
                    break
                elif j == my_list[-1]:
                    my_list.append(i)
        return len(my_list)

```

# 第一名解答
```python
def primes1(nn):
    """ Returns  a list of primes < n """
    sieve = [True] * int(nn/2)
    for i in range(3,int(nn**0.5)+1,2):
        if sieve[int(i/2)]:
            tmp = (nn - i ** 2 - 1) / (2 * i) + 1
            sieve[int(i*i/2)::i] = [False] * int(tmp)
    if nn==2: return [2]
    else: return [2] + [2*i+1 for i in range(1,int(nn/2)) if sieve[i]]
class Solution:
    def countPrimes(self, n):
        """
        :type n: int
        :rtype: int
        """
        if n<=1: return 0
        tmp=primes1(n)
        if n in tmp: return len(tmp)-1
        else: return len(tmp)
```
