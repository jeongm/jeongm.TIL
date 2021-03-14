## BufferedReader
- Scanner와 유사한 기능
- Scanner : Space, Enter 모두 경계로 인식
- BufferedReader : Enter만 경계로 인식, 입력받은 데이터가 String로 고정(때문에 입력받은 데이터의 형변환 작업이 필요한 경우가 많음)
- Scanner와 작업속도에 차이가 많이남 (BufferedReader가 더 빠름)
- 많은 양의 데이터를 입력받을 때 효율적
- 예외처리 필수 (보편적으로 throws IOException을 통해 예외처리함)
- import java.io.*; (import java.io.BufferedReader;)
### BufferedReader 사용법 
```java
BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
String s = br.readLine(); //string
int N = Integer.parseInt(br.readLine());  //int
```
```java
StringTokenizer st = new StringTokenizer(s);  // StringTokenizer 인자값에 입력 문자열 넣음
int a = Integer.parseInt(st.nextToken());
int b = Integer.parseInt(st.nextToken());

String array[] = s.split(" ");  // 공백마다 데이터 끊어서 배열에 넣음
```
## + throw 이용 시
- import java.io.IOException; 
- main 클래스 옆에 throws IOException를 작성필수. public static void main(String[] args) throws IOException{} 

## BufferedWriter
- System.out.println(); 과 유사한 기능
- 출력량이 많을 경우 효율적
```java
BufferedWriter bw = new BufferedWriter(new OutputStreamWriter(System.out));
String s = "helloworld";  
bw.Write(s + "\n"); //버퍼에 있는값 출력
bw.flush();   // 남아있는 데이터를 모두 출력시켜 버퍼를 비워줌
bw.close();   // 스트림을 닫아줌
```
- BuffereddWrite의 경우 버퍼를 잡아 놓았기 때문에 반드시 flush()/ close() 를 반드시 호출해 뒤처리를 해줘야 함
- System.out.println();과 달리 자동개행기능이 없기 때문에 개행이 필요한 경우 \n을 통해 따로 처리해줘야 함

## StringTokenizer
- 긴 문자열을 지정된 구분자를 기준으로 문자열을 슬라이싱하는데 사용됨
- 단 한개의 구분자 사용 가능
> ex) 10,20,30,40의 문자열을 ,구분자를 기준으로 슬라이싱하게 되면 4개의 문자열 획득 가능
```java
string A = "100,200,300,400";
StringTokenizer st = new StringTokenizer(a,",");    // String Tokenizer(String str, String delim) : 문자열을 지정된 구분자로 만드는 String Tokenizer를 생성 
                                                    //                                              구분자는 토큰으로 간주되지 않음
while(st.hasMoreToken()) {    // boolean hasMoreToken : 토큰이 남아있는지 알려줌
    System.out.println(st.nextToken());   // String nextToken() : 다음 토큰을 반환
}    
```
```
100
200
300
400
```
> 필요시 추가

### 연관된 문제 : 백준(15552번 : 빠른 A+B)
- https://www.acmicpc.net/problem/15552
```java
import java.io.*;
import java.util.*;

public class Main {

	public static void main(String[] args) throws IOException {
		// TODO Auto-generated method stub
		BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
		BufferedWriter bw = new BufferedWriter(new OutputStreamWriter(System.out));
		StringTokenizer st;		// 긴 문자열을 지정된 구분자를 기준으로 문자열을 슬라이싱 하는데 사용함

		int N = Integer.parseInt(br.readLine());
		
		for (int i = 0; i < N; i++) {
			st = new StringTokenizer(br.readLine());
			bw.write((Integer.parseInt(st.nextToken()) + Integer.parseInt(st.nextToken()))+ "\n");
		}
		bw.flush();
		bw.close();
	}

}

```
