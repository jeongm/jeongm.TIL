## java Scanner nextInt()사용 후 nextLine()사용시 문제점 해결
- java Scanner.nextInt()는 사용자 입력의 가장 마지막 개행문자(엔터 등) 입력 전까지만 입력받습니다.
- 마지막 개행문자를 제거하지 않기때문에 마지막에 입력된 개행문자는 아직 ~~버퍼에~~ 남아있습니다.
- 즉, nextInt()사용후 남아있는 개행문자가 다음 호출된 Scanner.nextLine()의 입력으로 처리되기 때문에 문제가 발생함 
```java
import java.util.Scanner;

public class test {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		Scanner sc = new Scanner(System.in);
		
		int a = sc.nextInt();	// 4 입력
		String word = sc.nextLine();  //개행문자가 처리됨
		
		System.out.println(a);
		System.out.println(word);	//nextInt()의 개행문자가 입력으로 처리됨
		
		sc.close();
	}
	
}
```
출력 : 
```
4
```
### 해결 방법1 : nextInt()사용 후 nextLine()추가
```java
    int a = sc.nextInt();	// 4 입력
		sc.nextLine();  // 개행문자 처리
		String word = sc.nextLine();  //hello 입력
		
		System.out.println(a);
		System.out.println(word);	
```

### 해결 방법2 : nextLine()으로 입력받은 후 Integer.parseInt()로 변환
```java
    int a;
		a= Integer.parseInt(sc.nextLine());	//nextLine()으로 입력받고 변환  //4 입력
    
		String word = sc.nextLine();  //hello 입력
		
		System.out.println(a);
		System.out.println(word);	
```
출력 : 
```
4
hello
```
