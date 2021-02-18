# 이진 탐색(binary search)
## 이진 탐색
- 이진 탐색을 사용하기 위해서는 배열의 데이터가 정렬되어 있어야 한다.
- 이진 탐색이 선형 탐색보다 빠름

```python
def bina_search(a: Sequence, key: Any) -> int:
    pl = 0                      # 맨 앞
    pr = len(a)-1               # 맨 끝
    
    while True:
        pc = (pl+pr)//2         # 중앙 값
        if key > a[pc] :        # key 값이 중앙 값보다 클때
            pl = pc+1           # pl값을 pc+1
        elif key == a[pc]:      # 검색 성공
            return pc           # 성공 인덱스 반환
        else:                   # key 값이 중앙 값보다 작을 때
            pr = pc - 1
        if pl > pr:             # pl이 pr보다 크면 안됨
            return -1           # 검색 실패
```

실행)
```python
n = int(input('몇 개의 데이터를 입력하시겠습니까? : '))
x = [None]*n
for i in range(len(x)):
    x[i] = int(input())
x.sort()

key = int(input('찾고 싶은 수: '))
idx = bina_search(x,key)
if idx == -1:
    print('값이 없습니다.')
else :
    print(f'찾으려는 값은 x[{idx}]에 있습니다.')
```
![실행결과]()
