## Scanner

```java
import java.util.Scanner; 
//혹은 import java.util.*;  java util라이브러리에 있는거 전부 import
public class JavaScanner{
 
    public static void main(String[] args) {
        
        Scanner sc = new Scanner(System.in);  //Scanner객체 생성
        int x;
        x = sc.nextInt();
        System.out.println(x);
        sc.close();
    }
 
}

```
- System.in을 사용하여 키보드 입력 값을 읽고 원하는 타입으로 변환하여 리턴함
