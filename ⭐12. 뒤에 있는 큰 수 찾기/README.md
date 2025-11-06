- https://school.programmers.co.kr/learn/courses/30/lessons/154539

```
def solution(numbers):
    answer = [-1]*(len(numbers)-1)
    result = [0]
    for i in range(1, len(numbers)):
        while True:
            if len(result) != 0:
                if numbers[i] > numbers[result[-1]]:
                    idx = result.pop()
                    answer[idx] = numbers[i]
                else:
                    result.append(i)
                    break
            else:
                result.append(i)
                break
        
    return answer + [-1]
```
