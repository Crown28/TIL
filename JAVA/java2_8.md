# 문제 2-8
2개의 실숫값을 입력받아 그 합과 평균을 구하는 프로그램을 작성하자.
```
import java.util.Scanner;

class SumAveDouble{
  public static void main(String[] args){
    Scanner stdIn = new Scanner(System.in);

    System.out.println("x값:");
    double x = stdin.nextDouble();

    System.out.print("y값:");
    double y = stdin.nextDouble();

    System.out.println("합계는 "+(x+y)+"입니다.");     
    System.out.println("평균은 "+(x+y)/2+"입니다.");
  }
}
```

###  next_메소드


|메소드|자료형|입력받을 수 있는 값|
|---|---|---|
|**nextBoolean()**|boolean|true 또는 false|
|**nextByte()**|byte|-128 ~ +127|
|**nextInt()**|int|-2147483648 ~ +2147483646|
|**nextDouble()**|double|1.79769313486231507E+374 ~ 4.94065645841246544E-324|
|**next()**|String|문자열(스페이스, 줄 바꿈 등으로 구분 가능)|
|**nextLine()**|String|한 줄의 문자열|

### next()와 nextLine()
문자열을 읽기 위해선 next 메소드를 사용한다. 단, next()를 사용한 키보드 입력에선 공백 문자나 탭 문자가 문자열을 나누게 된다. 공백 문자도 포함해서 한 줄의 입력을 문자열로 읽으려면 **nextLine** 메소드를 사용해야 한다. 

*출처 : 알쏭달쏭 자바 200제*