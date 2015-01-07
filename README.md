8 queen
======
Bloodly solved "Eight queens puzzle" by python.

``` python
import itertools

#https://github.com/deyuwang/8queen

def safe(pos) :
    for i in range(0,  7):
        for j in range(i + 1,  8):
            if abs(pos[j]  - pos[i]) == j - i : 
                return False
    return True

ps = itertools.permutations(range(1, 9),   8)

result = filter(safe,  ps)

print len(result) #92
```
