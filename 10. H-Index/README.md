- https://school.programmers.co.kr/learn/courses/30/lessons/42747#
```
def solution(citations):
    
    citations = sorted(citations, reverse = True)
    
    n = len(citations)
    i = citations[0]
    
    while True:
        answer = 0
        for j in citations:
            if j >= i:
                answer += 1

        if answer >= i:
            return i
        
        i -= 1
        
    if answer == 0:
        return n
```
