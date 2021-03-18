## Scanner

```java
import java.util.Scanner; 
//혹은 import java.util.*;  java util라이브러리에 있는거 전부 import
public class JavaScanner{
 
    public static void main(String[] args) {
        
        Scanner sc = new Scanner(System.in);  //Scanner객체 생성
        int x;
        x = sc.nextInt();  //입력받은 값을 정수로 변환해 저장
        System.out.println(x);
        
        String str;
        str = sc.nextLine();  // 문자열 입력받기
        System.out.println(str);
        
        sc.close(); //다쓰면 닫아야함 (누수 발생)
    }
 
}

```
- System.in을 사용하여 키보드 입력 값을 읽고 원하는 타입으로 변환하여 리턴함
