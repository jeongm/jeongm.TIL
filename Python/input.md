# [python] 데이터 여러개 입력받기(input)

### .split()이용해 데이터 여러개 입력받기
```python
data1 = input('숫자 입력: ').split()  # 입력값을 split()(공백)으로 구분
print(data)
print(type(data[0]))
```
```
실행 결과>
숫자 입력: 1 2 3 4 5
['1', '2', '3', '4', '5']
<class 'str'>
```
> str로 밖에 입력되지 않는 것 같음

```python
d1,d2 = input('문자 2번 입력 : ').split()
print(d1,d2)
print(type(d1))
```
```
실행 결과>
문자 2번 입력 : 1 2
1 2
<class 'str'>
```

### map이용해 데이터 입력받기
- 입력받은 값을 int형으로 바꿔줌
```python
data = map(int,input('숫자 입력: ').split())
print(data)
print(list(data))
```
```
실행 결과 >
숫자 입력: 1 2 3
<map object at 0x000001AE5EC033A0>
[1, 2, 3]
```
> 사실 잘 모르겠다(내용 추가 필요)
