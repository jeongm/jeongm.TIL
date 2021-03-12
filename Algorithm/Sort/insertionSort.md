## 삽입정렬(insertionSort)
- 삽입정렬은 전체 배열 중 정렬되어 있는 부분배열에 새 원소를 끼워넣는 일을 반복하는 방식으로 동작함

```java
package Sort;

public class insertionSort {
	public static void main(String[] args) {
		// TODO Auto-generated method stub
		int B[] = {4,7,2,3,8,0};
		
		for(int i = 1; i < B.length;i++) {
			int j = i;
			while(j > 0 && B[j-1]>B[j] ) // 앞의 친구가 나보다 크면 
			{
				int tmp = B[j];			//둘이 자리 바꿔줌
				B[j] = B[j-1];
				B[j-1] = tmp;
				--j;
			}
		}
	}
}

```
