- 효율성 문제 -> stack
```
'''
def call(s:str):
    end = 0
    s_re = ''
    for i in range(len(s)-1):
        if s[i] == s[i+1]:
            s_list = list(s)
            s_list[i] = ''
            s_list[i+1] = ''
            s_re = ''.join(s_list)
            #s_re = s[:i] + s[i+2:]
            print(s_re)
            end = 1
            break
    return s_re, end

def solution(s:str):
    s_re, end = call(s)
    
    if s_re == '':
        if end == 1:
            return 1
        else:
            return 0
    else:
        while True:
            s_re, end = call(s_re)
            if s_re == '':
                if end == 1: 
                    return 1 
                else:
                    return 0
            elif s_re != '':
                continue
'''
# stack
def solution(s:str):
    s_list = []
    for c in s:
        if s_list and s_list[-1] == c:
            s_list.pop()
            continue
        else:
            s_list.append(c)
            continue
    if len(s_list) != 0:
        return 0
    else:
        return 1
```
