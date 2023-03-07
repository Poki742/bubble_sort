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
## 설명<br>
### 1회전<br>
첫 번째 자료 7을 두 번째 자료 4와 비교하여 교환하고,<br>두 번째의 7과 세 번째의 5를 비교하여 교환하고,<br>세 번째의 7과 네 번째의 1을 비교하여 교환하고,<br>네 번째의 7과 다섯 번째의 3을 비교하여 교환한다.<br>이 과정에서 자료를 네 번 비교한다.<br>그리고 가장 큰 자료가 맨 끝으로 이동하므로 다음 회전에서는 맨 끝에 있는 자료는 비교할 필요가 없다.<br>
### 2회전<br>
첫 번째의 4을 두 번째 5와 비교하여 교환하지 않고,<br>두 번째의 5와 세 번째의 1을 비교하여 교환하고,<br>세 번째의 5와 네 번째의 3을 비교하여 교환한다.<br>이 과정에서 자료를 세 번 비교한다.<br>비교한 자료 중 가장 큰 자료가 끝에서 두 번째에 놓인다.<br>
### 3회전<br>
첫 번째의 4를 두 번째 1과 비교하여 교환하고,<br>두 번째의 4와 세 번째의 3을 비교하여 교환한다.<br>이 과정에서 자료를 두 번 비교한다.<br>비교한 자료 중 가장 큰 자료가 끝에서 세 번째에 놓인다.<br>
### 4회전<br>
첫 번째의 1과 두 번째의 3을 비교하여 교환하지 않는다.<br>
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

