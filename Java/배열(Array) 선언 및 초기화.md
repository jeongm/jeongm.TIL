## 배열(Array)이란?
- 배열(Array)이란 선형 자료구조 중 하나로, 동일한 타입의 연관된 데이터를 메모리에 연속적으로 저장하여 하나의 변수에 묶어서 관리하기 위한 자료구조
- 인덱스(Index)를 통해 데이터에 접근 가능
- 참조형 배열의 경우 배열에 저장되는 것은 객체의 주소이다.

## 배열(Array)선언 및 초기화
```java
// 크기, 초기화 없이 배열 참조변수만 생성
int[] arr;
int arr[];

//선언과 동시에 배열 크기 할당
int[] arr = new int[5];
String[] arr = new String[4];

//선언 및 초기화(크기지정)
int[] arr = new int[]{1,2,3,4,5};
int[] arr = {1,2,3,4,5};
String[] name = {"Kim", "Min", "Park", "Yi"};     // 원래 string은 클래스이므로 아래의 왼쪽처럼 new연산자를 통해 객체를 생성해야 한다.

```
## 배열의 출력
### _Arrays.toString(배열이름)_
 : 배열의 모든 요소를 '[첫번재 요소, 두번째 요소, ...]'로 만들어서 반환한다.
 > 배열의 요소를 쉽게 확인할 수 있음
 ```java
int[] score = {10,20,30,40};

System.out.println(Arrays.toString(score));
 ```
 출력:
 ```
 [10, 20, 30, 40]
 ```
 ### 만일 배열의 값을 바로 출력하면 어떻게 될까? 
  : __'타입@주소'__ 의 형식으로 출력됨
  ```java
  int[] score = {10,20,30,40};
  
	System.out.println(score);  // 배열을 가리키는 참조변수 score의 값을 출력한다. 
  ```
  출력:
  ```
  [I@7d4991ad   // 실행할 때 마다 달라질 수 있다.
  ```
  - '[I'는 1차원 int 배열이라는 의미이고
  - '@'뒤에 나오는 16진수는 배열의 주소인데 실제 주소가 아닌 내부 주소이다.

### 배열의 복사 : System.arraycopy()
 : 지정된 범위의 값들을 한 번에 통째로 복사
 ```java
 for(int i = 0; i < num.length; i++) { newNum[i] = num[i] }
                          ==
 System.arraycopy(num, 0, newNum, 0, num.length);
 // num[0]에서 new[0]으로 num.length개의 데이터를 복사
 ```
  
  
## +
```java
char[] hex = {'C','A','F','F'};
		
System.out.println(new String(hex));  //hex를 새로 string으로 저장 출력

```
  
