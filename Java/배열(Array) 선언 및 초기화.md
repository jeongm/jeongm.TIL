## 배열(Array)이란?
- 배열(Array)이란 선형 자료구조 중 하나로, 동일한 타입의 연관된 데이터를 메모리에 연속적으로 저장하여 하나의 변수에 묶어서 관리하기 위한 자료구조
- 인덱스(Index)를 통해 데이터에 접근 가능

## 배열(Array)선언 및 초기화
```java
// 크기, 초기화 없이 배열 참조변수만 생성
int[] arr;
int arr[];

//선언과 동시에 배열 크기 할당
int[] arr = new int[5];
String[] arr = new String[8];

//선언 및 초기화(크기지정)
int[] arr = new int[]{1,2,3,4,5};
int[] arr = {1,2,3,4,5};
int[] string = {"A","B","C","D"};
```
