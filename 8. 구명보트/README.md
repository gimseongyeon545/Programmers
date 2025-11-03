- https://school.programmers.co.kr/learn/courses/30/lessons/42885#

```
def solution(people, limit):
    people = sorted(people, reverse = True)
    cnt = 0
    
    n = len(people)
    j = n-1
        
    for idx, i in enumerate(people):
        if idx == j:
            cnt +=1
            break
        else:
            if people[j] + i <= limit:
                cnt += 1
                if (idx+1 == j):
                    return cnt
                j -= 1
            elif people[j] + i > limit:
                cnt += 1
                continue
    
    return cnt
```
