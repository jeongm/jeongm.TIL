# 선형검색(=순차검색, Linear Search)
## 선형검색
: 데이터가 모인 집합(배열, 링크드리스트 등)의 처음부터 끝까지 하나씩 순서대로 비교하며 원하는 값을 찾아내는 알고리즘으로
주로 원소의 값이 정렬되지 않는 배열에서 검색할 때 사용하는 유일한 방법이다.
선형 검색은 반복할 때마다 2가지 종료 조건을 체크함
- 시간 복잡도 : O(n)

```python
def lin_search(x: Sequence, key:Any) -> int:
    for i in range(len(x)):         
        if key == x[i]:        # 검색 성공
            return i           # 인덱스 반환
    else :
        return -1              # 검색 실패 
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
```
찾고싶은 정수를 입력하세요. :5
5는 x[1]에 있습니다.
```

### 시간 복잡도 계산
```python
def lin_search(x: Sequence, key:Any) -> int:
    for i in range(len(x)):  # 실행 횟수 : n/2  복잡도 : O(n)
        if key == x[i]:      # 실행 횟수 : n/2  복잡도 : O(n)
            return i         # 실행 횟수 : 1    복잡도 : O(1)
    else :
        return -1            # 실행 횟수 : 1    복잡도 : O(1)
```
- 시간 복잡도 : O(n)
- O(n)에 필요한 계산시간은 n에 비례
- 이와 같이 n에 비례하는 횟수만큼 실행되는 경우의 복잡도는 O(n)으로 나타냄

## 보초법(Sentinel Method)
: 검색하고자 하는 key값을 맨 끝에 넣어 비용을 줄임(종료조건이 필요 없음)
이때 저장하는 값을 '보초'라고 함

```python
def lin_search2(x: Sequence, key: Any) -> int:
    a = copy.deepcopy(x)        # x를 복사
    a.append(key)               # 보초 key 추가
    
    i=0
    while True:
        if a[i] == key:
            break
        i+=1
    return -1 if i == len(x) else i
```
