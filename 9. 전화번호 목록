- https://school.programmers.co.kr/learn/courses/30/lessons/42577
```
'''
def solution(phone_book): 
    for i in phone_book: 
        for j in phone_book: 
            if i != j: 
                if i == j[:len(i)]: 
                    return False 
                    exit(0) 
                else: continue 
    return True
'''



def solution(phone_book):
    phone_book = sorted(phone_book)
    
    for idx, i in enumerate(phone_book[:-1]):
        if phone_book[idx] == phone_book[idx+1][:len(phone_book[idx])]:
            return False
        else:
            continue
    return True
```
