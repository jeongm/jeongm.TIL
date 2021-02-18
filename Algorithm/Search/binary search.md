# 이진 탐색(binary search)
## 이진 탐색
- 이진 탐색을 사용하기 위해서는 배열의 데이터가 정렬되어 있어야 한다.
- 이진 탐색이 선형 탐색보다 빠름

```python
def bina_search(a: Sequence, key: Any) -> int:
    pl = 0
    pr = len(a)-1  
    
    while True:
        pc = (pl+pr)//2
        if key > a[pc] :
            pl = pc+1
        elif key == a[pc]:
            return pc
        else: 
            pr = pc - 1
        if pl > pr:
            return -1
```
