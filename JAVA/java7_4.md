# 문제 7-4
1부터 n까지의 정수의 합을 구해서 반환하는 메서드를 작성하자.

```
import java.util.Scanner;

class Min3 {
	static int min(int n) {
		int sum = 0;
		for(int i=1; i<=n; i++)
			sum = sum + i;
		return sum;
	}
	
	public static void main(String[] args) {
		Scanner scanner = new Scanner(System.in);
		
		int x;
		
		do {
			System.out.print("x의 값:");
			x = scanner.nextInt();
		} while(x<=0);
		
		System.out.println(x+"까지의 합은"+min(x));
	}
}
```

