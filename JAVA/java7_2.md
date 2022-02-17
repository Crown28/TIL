# 문제 7-2
3개의 int형 인수 a,b,c중 최솟값을 구하는 min 메서드를 작성하자.

```
import java.util.Scanner;

class Min3 {
	static int min(int a, int b, int c) {
		int min = a;
		if(b<min) min = b;
		if(c<min) min = c;
		return min;
	}
	public static void main(String[] args) {
		Scanner scanner = new Scanner(System.in);
		System.out.print("정수a:");
		int a = scanner.nextInt();
		System.out.print("정수b:");
		int b = scanner.nextInt();
		System.out.print("정수c:");
		int c = scanner.nextInt();
		System.out.println("최솟값은"+min(a,b,c));
	}
}
```

## 메서드, 인수, 변수의 이름
min 메서드는 매개 변수 a,b,c에 입력한 3개 값 중 최솟값을 구하는 메서드이다. 메서드 내에서 선언한 변수 min은 메서드명과 같지만 메서드명과 변수는 종류가 다르므로 식별자가 같아도 충돌하지 않는다. 반면 메서드 블록 내에선 매개 변수와 같은 이름의 변수는 선언할 수 없다.<br><br>

min 메서드는 3개의 인수를 받는다. 매개 변수가 여러 개인 경우는 쉼표로 구분해 선언하며 호출하는 인수도 쉼표로 구분한다. main 메서드의 변수 a,b,c와 min메서드의 매개변수 a,b,c는 동일한 이름을 사용하지만, 서로 다른 변수이다. min 메서드가 호출될 때, 매개 변수 a,b,c가 main 메서드의 a,b,c의 값으로 초기화된다.

*출처 알쏭달쏭 자바 200제*
