# ArrayList

ArrayList는 List인터페이스를 상속받은 클래스로 *크기가 가변적으로 변하는 선형리스트*이다,
일반적인 배열과 같은 순차리스트이며 인텍스로 내부의 객체를 관리한다는 점등이 유사하지만 한번 생성되면 크기가 변화지 않는 배열과는 달리 ArrayList는 객체들이 추가되어 저장 용량은 초과한다면 자동으로 부족한 크기만큼 저장용량이 늘어남

## ArrayList 사용법 - 선언
```java
import java.util.ArrayList;
...

ArrayList alist = new ArrayList();  // 타입 미설정 시 object로 선언됨
ArrayList<Integer> num = new ArrayList<Integer>();  
ArrayList<Integer> num = new ArrayList<>(); 
ArrayList<Integer> num = new ArrayList<Integer>(5); // 크기 설정 가능
ArrayList<Integer> num = new ArrayList<Integer>(Array.asList(0,1,2));  // 초기화

```

### 값 추가, 제거
```java
ArrayList<Integer> alist = new ArrayList<Integer>();
alist.add(3); //값 추가
alist.add(null); //null값도 add가능
alist.add(1,10); //alist[1]에 10 삽입

alist.remove(1);  //alist[1] 제거, .remove(index)
alist.clear();  //모든 값 제거

System.out.println(alist.size());
```
```java
ArrayList<Student> members = new ArrayList<Student>();  //객체도 가능
Student student = new Student(name,age);
members.add(student);   
members.add(new Member("홍길동",15));
```
ArrayList에 값을 추가하려면 ArrayList의 add(index, value) 메소드를 사용하면 됩니다.    
index를 생략하면 ArrayList 맨 뒤에 데이터가 추가되며 index중간에 값을 추가하면 해당 인덱스부터 마지막 인덱스까지 모두 1씩 뒤로 밀려납니다. 


### 값 가져오기
```java
alist.get(2);
```
특정 인덱스에 위치한 엘리먼트를 가져올 때 사용. 
### 검색
```java
ArrayList<Integer> alist = new ArrayList<Integer>(Arrays.asList(1,2,3));
alist.contains(1); //alist에 1이 있는지 검색 있으면 true 없으면 false
alist.indexOf(1); //1이 있는 index반환 없으면 -1
```

### 출력
```java
System.out.println(alist.get(0));//0번째 index 출력

Iterator iter = alist.iterator(); //Iterator 선언 
while(iter.hasNext()){//다음값이 있는지 체크
    System.out.println(iter.next()); //값 출력
}

//for문출력도있지만 다 아니까 생략
```
