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
