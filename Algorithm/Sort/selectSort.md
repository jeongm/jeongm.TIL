## 선택 정렬(selectSort)
- 모든 i에 대해 A[i..N-1]에서 가장 작은 원소를 찾은 뒤, 이것을 A[i]에 넣는 것을 반복함

### 과정 설명
- 주어진 배열 중에서 최솟값을 찾는다.
- 그 값을 맨 앞에 위치한 값과 교체한다(패스(pass)).
- 맨 처음 위치를 뺀 나머지 리스트를 같은 방법으로 교체한다.
- 하나의 원소만 남을 때까지 위의 1~3 과정을 반복한다.


```java
package selectionSort;

public class selectionSort {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		
		int A[] = {4,7,2,3,8,0}; 
		
		for(int i = 0; i < A.length-1; i++) {
			int mini = i;
			for(int j = i+1; j < A.length; j++) {
				if(A[mini] > A[j])
					mini = j;
			}
			int tmp = A[i];
			A[i] = A[mini];
			A[mini] = tmp;	
		}	// 시간복잡도 : O(n^2)
		
		for(int i = 0 ;i < A.length;i++) {
			System.out.println(A[i] + " ");
		}
		
		System.out.println();
	}

}

```
