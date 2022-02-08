# 문제 4-5
입력받은 정숫값부터 0까지 카운트다운하는 프로그램을 작성하라. 카운트다운 종류 후의 변숫값을 확인할 수 있게 할 것.

```
import java.util.Scanner;

public class EnumScope {

	public static void main(String[] args) {
		Scanner scanner = new Scanner(System.in);
		int a;
		do {
		System.out.println("양의 정숫값 입력");
		a = scanner.nextInt();
		}while (a<=0);
		
		while(a>=0) {
			System.out.println(a--);
		}	
	}
}
```
> while(a>=0) {<br>
			System.out.println(a);<br>
			a = a-1;<br>
		}

다음과 같은 코드를 간결하게 바꿀 수 있음

> while(a>=0) {<br>
			System.out.println(a--); //x의 값을 표시한 후 감소시킴<br>
		}	


> while(a>=0) {<br>
			System.out.println(--a); //x의 값을 감소시킨 후 표시<br>
		}	

