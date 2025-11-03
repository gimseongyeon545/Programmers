- Counter 뺄셈

```
from collections import Counter
def solution(want, number, discount):
    idx_max = len(discount) - 10
    counter = Counter(discount[:10])
    idx = 0
    answer = 0
    
    need = Counter(dict(zip(want, number)))
    
    while idx <= idx_max:
        if idx != 0:
            counter[discount[idx-1]] -= 1
            if discount[idx+9] in counter.keys():
                counter[discount[idx+9]] += 1
            else: counter[discount[idx+9]] = 1
        
        if need-counter == {}:
            answer += 1
        idx +=1 
    return answer
```
