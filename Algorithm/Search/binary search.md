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
            return -1           # 검색 실패 -1반환
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
```
몇 개의 데이터를 입력하시겠습니까? : 5
33
22
44
55
11
찾고 싶은 수: 33
찾으려는 값은 x[2]에 있습니다.
```
### 시간 복잡도
```python
def bina_search(a: Sequence, key: Any) -> int:
    pl = 0                     # 실행 회수 : 1    복잡도: O(1)
    pr = len(a)-1              # 실행 회수 : 1    복잡도: O(1)
    
    while True:               
        pc = (pl+pr)//2        # 실행 회수 : logn    복잡도: O(logn)
        if key > a[pc] :       # 실행 회수 : logn    복잡도: O(logn)
            pl = pc+1          # 실행 회수 : logn    복잡도: O(logn)
        elif key == a[pc]:     # 실행 회수 : logn    복잡도: O(logn)
            return pc          # 실행 회수 : 1    복잡도: O(1)
        else:                  
            pr = pc - 1        # 실행 회수 : logn    복잡도: O(logn)
        if pl > pr:            # 실행 회수 : logn    복잡도: O(logn)
            return -1         # 실행 회수 : 1    복잡도: O(1)
```
- 시간 복잡도 : 이진 검색 알고리즘은 반복할 때마다 검색 범위가 거의 절반으로 줄어드므로
- 평균: logn, 실패 시: log(n+1), 성공: log n-1
