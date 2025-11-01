- https://school.programmers.co.kr/learn/courses/30/lessons/12982
- `itertools.combinations` 시간초과 해결법
- sort 후 누적합

```
'''
from itertools import combinations as comb
def solution(d: list, budget: int):
    length = len(d)
    for i in range(length, 0, -1):
        combs = list(comb(d, i))
        for j in combs:
            if sum(j) <= budget:
                answer = i
                return answer
'''

def solution(d: list, budget: int):
    d = list(sorted(d))
    a = 0
    for idx, i in enumerate(d):
        if a + i == budget:
            return idx+1
        elif a+i > budget:
            return idx
        elif a+i < budget:
            a += i
            if idx == len(d)-1:
                return idx+1
```
