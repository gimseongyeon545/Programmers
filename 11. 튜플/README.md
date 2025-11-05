- https://school.programmers.co.kr/learn/courses/30/lessons/64065
```
from collections import Counter as counter
def solution(s):
    max_len = 0
    s = s[2:-2]
    
    list_s = s.split('},{')
    answer = []
    
    for i in list_s:
        a = i.split(',')
        a = list(map(lambda i:int(i), a))
        answer.append(a)
    
    result = counter()
    
    for i in answer:
        result += counter(i)
    return sorted(result, key=result.get, reverse=True)

```
