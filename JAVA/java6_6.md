# 문제 6-6
배열의 요소 수와 개별 요소의 값을 입력 받아서 표시하는 프로그램을 작성하자. 표시 형식은 배열 초깃값과 같은 형식으로, 각 요소의 쉼표를 연결하고 {}로 감싼 형태이다.

```
import java.util.Scanner;

class PrintArray{
  public static void main(String[] args){
    Scanner scanner = new Scanner(System.in);

    System.out.print("요소 수:");
    int n = scanner.nextInt();
    int[]a = new int[n];

    for (int i = 0; i<n; i++){
      System.out.print("a[" + i + "]=");
      a[i] = scanner.nextInt();
    }
    System.out.print("a = {");
    if (n>=2)
    	for(int i=0; i<n-1; i++)
    		System.out.println(a[i]+", ");
    if (n>=1)
    	System.out.print(a[n-1]);
    System.out.print("}");
  }
}
```

## 실행 예
```
요소 수:3
a[0] = 5
a[1] = 7
a[2] = 8
a = {5,7,8}
```
---
## 초깃값 형식으로 출력
요소를 쉼표로 연결해서 표시한다. 숫자와 쉼표의 개수가 다르므로 프로그램이 복잡한 편이다. 요소수의 수가 0이면 숫자와 쉼표 모두 0개, 그렇지 않으면 쉼표의 개수는 요소 수보다 1개 작다.<br>

*출처 알쏭달쏭 자바 200제*