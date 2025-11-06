- https://school.programmers.co.kr/learn/courses/30/lessons/42578#
- (a+1) * (b+1) * ... - 1
```
from collections import Counter as counter
from math import prod

def solution(clothes):
    counter_cloth = counter()
    
    for val, key in clothes:
        if key in counter_cloth.keys():
            counter_cloth[key] +=1
        else:
            counter_cloth[key] = 2
    
    return prod(counter_cloth.values())-1
```
