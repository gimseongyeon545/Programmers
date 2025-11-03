- https://school.programmers.co.kr/learn/courses/30/lessons/42842

```
def solution(brown, yellow):
    if yellow == 1:
        width, i = 1, 1
        if (width + 2) * (i + 2) == (brown + yellow):
            return [width+2, i+2]
    
    for i in range(1, yellow):
        if yellow % i == 0:
            width = yellow // i
            if (width + 2) * (i + 2) == (brown + yellow):
                return [width+2, i+2]
        else:
            continue
```
