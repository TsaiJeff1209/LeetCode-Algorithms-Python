# Unique Morse Code Words

## 2018/4/7 beats 93.72 % of python3
### Spend 40 ms
```python
class Solution:
    def uniqueMorseRepresentations(self, words):
        """
        :type words: List[str]
        :rtype: int
        """
        def WordtoMorse(word):
            morse = [".-","-...","-.-.","-..",".","..-.","--.","....","..",".---","-.-",".-..","--","-.","---",".--.","--.-",".-.","...","-","..-","...-",".--","-..-","-.--","--.."]
            m = ""
            for i in word:
                m = m + morse[ord(i)-97]
            return m
        my_list = []
        for word in words:
            my_list.append(WordtoMorse(word))
        return len(set(my_list))
```
