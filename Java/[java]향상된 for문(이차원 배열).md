### for문
```java
for(초기화 ; 조건식 ; 증감식) {
  //수행할 문장
}
```

### 향상된 for문
- 수와 배열의 타입은 같아야 하며,
- 배열에 저장된 값이 매 반복마다 하나씩 순서대로 읽혀서 변수에 저장됨
- 읽어오는 용도로 사용

```java
for( 타입 변수명 : 배열) {
        System.out.println(변수명);
}
```
ex)
```java
public class ArrayEx18 {
  public static void main(String[] args) {
    int [][] score = {
            {100,100,100},
            {20,20,20},
            {30,30,30},
            {40,40,40}
    };
    
    for(int [] tmp : score) {
      for(int i : tmp) {
        System.out.print(i + "  ");
      }
    }
  }
}
```
출력>
```
100  100  100  20  20  20  30  30  30  40  40  40
```
