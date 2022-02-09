# 문제 4-4
2개의 정숫값을 읽어서 두 정수 사이에 있는 모든 정숫값을 작은 것부터 큰 순으로 표시하는 프로그램을 작성하자.

```
import java.util.Scanner;

public class EnumScope {

	public static void main(String[] args) {
		Scanner scanner = new Scanner(System.in);
		System.out.println("A값 입력");
		int a = scanner.nextInt();
		System.out.println("B값 입력");
		int b = scanner.nextInt();
		
		if(a>b) {
			int t = a;
			a = b;
			b = t;
		}

		do {
			System.out.println(a+" ");
			a = a + 1;
		}while (a <= b);
		System.out.println();		
	}
}
```
* a<=b가 되도록 a와 b를 정렬
  * 변수 a와b에 어떤 값이 입력될지는 아무도 모른다. 따라서 두 변수의 대소 관계는 실제로 입력된 시점에 결정된다.
* a이상 b이하의 모든 정수를 순서대로 표시
  * a이상 b이하의 모든 정수를 순서대로 표시한다. 이를 위해서 다음과 같은 처리를 a가 b이하인 동안에 반복한다.
    * a의 값을 표시한다.
    * a의 값을 1씩 증가시킨다(a에 1을 더한 값을 a에 다시 대입한다).
  
*출처 : 알쏭달쏭 자바 200제*