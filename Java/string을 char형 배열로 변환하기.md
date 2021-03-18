## String형 배열을 char형 배열로 변환하기 : *toCharArray()*
String형 배열을 char형으로 변환해 하나씩 저장
```java
String word = "hello";
char[] array_word;
		
array_word = word.toCharArray();
		
for(int i = 0; i < array_word.length;i++) {
		System.out.println(array_word[i]);
 }
```
출력:
```
h
e
l
l
o
```

## String클래스의 주요 메서드
- char charAt(int index) : 문자열에서 해당 위치(index)에 있는 문자를 반환한다. (ex char ch = str.charAt(3))
- int length() : 문자열의 길이를 반환한다.
- String substring(int from, int to) : 문자열에서 해당 범위(from~to)에 있는 문자를 반환(to는 범위에 포함되지 않음)
- boolean equals(Object obj) : 문자열의 내용이 obj와 같은지 확인한다. (같으면 ture, 다르면 false)(대소문자 구분함)
- boolean equalsIgonoreCase() : equals와 같은데, 대소문자를 구분하지 않음
- substring() : 문자열의 일부를 뽑아올 수 있음(ex String tmp = str.substring(1,4))
- char[] toCharArray() : 문자열을 문자배열(char[])로 변환해서 반환한다.
> charAt에서드는 문자열에서 지정된 index에 있는 한 문자를 가져옴
