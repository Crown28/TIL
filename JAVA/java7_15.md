# 문제 7-15
배열 a가 가진 모든 요소의 합을 구하는 sumOf() 메서드를 작성하자.

```
import java.util.Scanner;

public class SumOf1 {
	static int sumOf(int[] a) {
		int sum = 0;
		for(int i=0; i<a.length; i++)
			sum+=a[i];
		return sum;
	}
	
	public static void main(String[] args) {
		Scanner scanner = new Scanner(System.in);
		
		System.out.print("요소 수:");
		int num = scanner.nextInt();
		int[] x = new int[num];
		
		for(int i=0; i<num; i++) {
			System.out.print("x["+i+"]:");
			x[i] = scanner.nextInt();
		}
		System.out.println("모든 요소 합은 "+sumOf(x));
	}
}
```

## 배열을 받는 메서드
배열이 가진 모든 요소의 합을 구하는 문제다. main 메서드에선 요소 수를 읽어 배열을 생성하고 각 요소의 값을 읽는다. 그리고 sumOf 메서드를 호출해서 입력한 배열 요소의 합계를 구해서 반환한다. 배열을 매개 변수로 받을 때는 int[] a처럼 일반적인 배열 선언 방식을 사용한다.