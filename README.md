# bubble_sort<br>
## 버블 정렬(bubble sort) 알고리즘의 개념 요약<br>

서로 인접한 두 원소를 검사하여 정렬하는 알고리즘<br>
인접한 2개의 레코드를 비교하여 크기가 순서대로 되어 있지 않으면 서로 교환한다.<br>
선택 정렬과 기본 개념이 유사하다.<br>
## 장점과 단점<br>
장점 구현이 매우 간단, 소스코드가 직관적 제자리 정렬 → 공간복잡도 O(n) ...<br>
단점 시간복잡도가 최악, 최선, 평균 모두 O(n^2)으로, 굉장히 비효율적 특정 요소가 최종 정렬 위치에 있는 경우라도 교환이 일어남<br>
## 예시<br>
![image](https://user-images.githubusercontent.com/126844692/223324892-77800a8c-f9a1-4093-8051-bbf265a095f9.png)<br>
## for문<br>

package 자바;
import java.util.Arrays;
public class bubble_sort {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		System.out.println("[버블정렬(bubble sort) - 이중 for문을 사용해 오름차순(작은순서) 데이터 정렬 실시]");	
		int data[] = {5,4,3,2,1};
		System.out.println("원본 : "+Arrays.toString(data));		
		int save = 0;
			for(int i=1; i<=5; i++) { //정렬 회차 정의 실시			
				for(int k=0; k<data.length; k++) { //정렬 회차당 배열 전체 데이터를 다시 정렬한다
					if((k+1) < data.length) { //배열 길이를 벗어나지 않도록 조건을 건다
						if(data[k] > data[k+1]) {
							save = data[k];
							data[k] = data[k+1];
							data[k+1] = save;
					}	
				}				
			}			
			System.out.println(i+" 회전 정렬 : "+Arrays.toString(data));	
		}
	}

}

## 출력 결과<br>
[버블정렬(bubble sort) - 이중 for문을 사용해 오름차순(작은순서) 데이터 정렬 실시]<br>
원본 : [5, 4, 3, 2, 1]<br>
1 회전 정렬 : [4, 3, 2, 1, 5]<br>
2 회전 정렬 : [3, 2, 1, 4, 5]<br>
3 회전 정렬 : [2, 1, 3, 4, 5]<br>
4 회전 정렬 : [1, 2, 3, 4, 5]<br>
5 회전 정렬 : [1, 2, 3, 4, 5]<br>
## 실행된 이미지<br>
![image](https://user-images.githubusercontent.com/126844692/223325783-ccfadc6e-911a-42ed-a2ba-4d69f8334b6b.png)

