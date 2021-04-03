# n개의 원소 중 m개를 고르는 모든 조합을 찾는 알고리즘
```python
def pick(n, m, picked):

    if m == 0:
        print(picked)

    if not picked:
        last = 0
    else :
        last = picked[len(picked)-1]+1

    for i in range(last, n):
        picked.append(i)
        pick(n, m - 1, picked)
        del picked[len(picked) - 1]

if __name__ == '__main__':
    a = []
    n = int(input())
    m = int(input())
    pick(n, m, a)


```
이 코드는 텅 빈 답에서 시작해서 매 단계마다 하나의 원소를 추가하는 일을 반복하다가,    
하나의 답을 만든 뒤에는 이전으로 돌아가 다른 원소를 추가하는 식으로 모든 답을 생성함
때문에 재귀 호출은 완전 탐색을 구현할 때 아주 유용한 도구이다.
