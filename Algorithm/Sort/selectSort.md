## 선택 정렬(selectSort)
- 모든 i에 대해 A[i..N-1]에서 가장 작은 원소를 찾은 뒤, 이것을 A[i]에 넣는 것을 반복함

```java
package selectionSort;

public class selectionSort {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		
		int A[] = {4,7,2,3,8,0}; 
		
		for(int i = 0; i < A.length; i++) {
			int mini = i;
			for(int j = i+1; j < A.length; j++) {
				if(A[mini] > A[j])
					mini = j;
			int tmp = A[i];
			A[i] = A[mini];
			A[mini] = tmp;	
			}
		}
		
		for(int i = 0 ;i < A.length;i++) {
			System.out.println(A[i] + " ");
		}
		
		System.out.println();
	}

}

```
