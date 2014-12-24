8 queen
======
Bloodly solved "Eight queens puzzle" by python.

``` python
import itertools

def safe(pos) :
    for i in range(0,  8-1):
        for j in range(i + 1,  8):
            if abs(pos[j]  - pos[i]) == abs(j - i) : 
                return False
    return True
 
result = filter(safe,  itertools.permutations(range(1, 8+1),   8))

print len(result) #92
```
