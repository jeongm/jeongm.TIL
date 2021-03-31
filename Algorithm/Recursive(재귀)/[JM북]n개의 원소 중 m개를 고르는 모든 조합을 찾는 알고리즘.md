# n개의 원소 중 m개를 고르는 모든 조합을 찾는 알고리즘
```java
import java.util.*;

public class Main {
	// n: 전체 원소의 수
	// picked : 지금까지 고른 원소들의 번호
	// toPick : 더 고를 원소의 수
	// 일 때, 앞으로 toPick개의 원소를 고르는 모든 방법을 출력한다.
	static void pick(int n, ArrayList<Integer> picked, int toPick)
	{
		// 기저 사례 : 더 고를 원소가 없을 때 고른 원소들을 출력한다.
		if( toPick == 0) {
			for(int pick : picked) {
				System.out.print(pick);
			}System.out.println();
		}
		// 고를 수 있는 가장 작은 번호를 계산한다.
		int smallest = picked.isEmpty() ? 0 : picked.get(picked.size()-1) + 1;	// picked가 비어있으면 0, 아니면 가장작은친구 가져옴

		// 이 단계에서 원소 하나를 고른다.
		for(int next = smallest; next < n; ++next) {
			picked.add(next);
			pick(n,picked,toPick-1);
			picked.remove(picked.size()-1);
		}
	}
	
	public static void main(String[] args) {
		// TODO Auto-generated method stub
		Scanner sc = new Scanner(System.in);
		
		int n = sc.nextInt(); // 전체 원소의 수
		int m = sc.nextInt();	// 출력하고 싶은 원소의 수
		
		ArrayList<Integer> alist = new ArrayList<Integer>();
		pick(n,alist,m);
		
		sc.close();
	}
	
}

```
이 코드는 텅 빈 답에서 시작해서 매 단계마다 하나의 원소를 추가하는 일을 반복하다가,    
하나의 답을 만든 뒤에는 이전으로 돌아가 다른 원소를 추가하는 식으로 모든 답을 생성함
때문에 재귀 호출은 완전 탐색을 구현할 때 아주 유용한 도구이다.
