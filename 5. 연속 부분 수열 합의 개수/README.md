- https://school.programmers.co.kr/learn/courses/30/lessons/131701
- 원형 리스트
```
def solution(elements):
    answer = []
    n = len(elements)
    for i in range(2, n+1):
        for j in range(n):
            idx = (i+j) % n
            if i+j >= n:
                answer.append(sum(elements[j:]) + sum(elements[:idx]))
            else: answer.append(sum(elements[j:idx]))
            
    return len(set(answer+elements))
```
