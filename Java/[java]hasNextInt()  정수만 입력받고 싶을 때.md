### hasNextInt()   
- 정수 입력 시 true를 반환하고 그렇지 않은 경우 false를 반환합니다.
```java
import java.util.*;

public class Main {

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        
        int A, B;
        
        while(sc.hasNextInt())    //sc.hasNextInt() 입력한 숫자가 정수면 true 아니면 false
        {
            A = sc.nextInt();
            B = sc.nextInt();
            
            System.out.println(A+B);
        }
        
        sc.close();
    }
}
```
