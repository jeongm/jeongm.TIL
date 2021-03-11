## print 와 println (+printf)
system.out.println()은 문자를 출력 후 다음줄로 넘어갑니다(줄띄어쓰기).

system.out.print()는 줄띄어씌기가 되지 않고 그래도 출력됩니다.

즉 println은 print + \n으로 볼 수 있습니다.

주로 println을 쓰며 줄띄어쓰기가 필요없는 경우 print를 씁니다.


예시)
```java
System.out.println("Hello world");
System.out.println("My name is");
System.out.println("jeong");

System.out.print("Hello world");
System.out.print("My name is");
System.out.print("jeong");
```
```
Hello world
My name is
jeong
Hello worldMyname isjeong
```
## printf

System.out.printf()

printf는 지시자를 통해 변수의 값을 여러가지 값으로 출력할 수 있다.

c언어의 printf와 같은 역할을 한다.


여기서 지시자는 %d, %f, %c, %s 등을 말한다.

 

예시)
```java
System.out.printf("num = %d\n", num);
```
출력>
```
num = 8
```


