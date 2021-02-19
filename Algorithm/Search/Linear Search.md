# 선형검색(=순차검색, Linear Search)
## 선형검색
: 데이터가 모인 집합(배열, 링크드리스트 등)의 처음부터 끝까지 하나씩 순서대로 비교하며 원하는 값을 찾아내는 알고리즘으로
주로 원소의 값이 정렬되지 않는 배열에서 검색할 때 사용하는 유일한 방법이다.
선형 검색은 반복할 때마다 2가지 종료 조건을 체크함
- 시간 복잡도 : O(n)

```python
def lin_search(x: Sequence, key:Any) -> int:
    for i in range(len(x)):
        if key == x[i]:
            return i
    else :
        return -1
```
<실행>
```python
a = [1,5,88,3,4,6]

ky = int(input('찾고싶은 정수를 입력하세요. :'))

idx = lin_search(a,ky)

if idx == -1:
    print('검색 실패: 찾으려는 값이 없습니다.')
else:
    print(f'{ky}는 x[{idx}]에 있습니다.')

```

## 보초법(Sentinel Method)
: 검색하고자 하는 key값을 맨 끝에 넣어 비용을 줄임(종료조건이 필요 없음)
이때 저장하는 값을 '보초'라고 함
