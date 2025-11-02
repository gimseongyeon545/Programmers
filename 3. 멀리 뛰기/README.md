- 피보나치 수열
- bottom up 방식

```
def solution(n):
    cnt = 0
    if n == 1:
        return 1
    else:
        a, b = 1, 2
        
        while cnt < n-2:
            a_ = b
            b = a+b
            a = a_
            cnt += 1
            
    return b %1234567
```
